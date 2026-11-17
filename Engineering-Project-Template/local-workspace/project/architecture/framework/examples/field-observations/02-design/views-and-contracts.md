# Field observations, part 2 — views and contracts

Scope CTX-01 includes the device capture logic, local journal, ingest and operator-facing history. The radio network, inspector, duty operator and equipment authority are external actors or dependencies. The diagram uses arrows for the named interaction. The reverse receipt has its own contract.

~~~text
Inspector -- submits reading --> Device journal -- IF-01 upload --> Ingest ledger
Inspector <-- local receipt ---- Device journal <-- IF-02 receipt -- Ingest ledger
Duty operator <-- age and disposition -- History <-- committed event -- Ingest ledger
~~~

| Element | Authority and retained state | Interrupted behavior |
| --- | --- | --- |
| Device journal | Assigns device generation and sequence, stores payload before local receipt | Recovers locally acknowledged items on restart and retries until remote disposition |
| Ingest ledger | Validates enrollment, stores one canonical record per identity and pending publication atomically | Returns the recorded outcome for an equivalent duplicate |
| History | Owns the projection and its processed identity ledger | Replays a committed event without creating a second effect |
| Duty operator | Reviews age, uncertain time, gaps and conflicts | Can escalate a concern to the separate equipment authority |

**IF-01.** Carry device identity, boot or commissioning generation as specified by the identity contract, durable sequence, payload, units, schema version, observed time, time confidence and content digest. The authenticated enrollment binds the device to a site. The key space must prevent a reset or replacement from reusing an old observation key. In this case commissioning assigns the generation and a normal reboot preserves it and the sequence.

**IF-02.** Ingest sends a committed receipt after the validated record and publication intent commit together. A device may reclaim an item after verifying a matching committed receipt. A conflict or quarantine requires explicit disposition and retained custody. A duplicate receipt for an already-reclaimed item has no new effect. The protocol defines recovery lookup for an acknowledgment lost in transit.

## Runtime walk

1. Unplug the network. A record becomes locally accepted only after durable commit. Authority for retaining the sole copy is now at the device.
2. Restore the network. Ingest verifies identity, authorization, schema and content before commit. The record may arrive more than once. A reused key with incompatible content is quarantined for investigation.
3. Interrupt the connection after remote commit. Retry returns the existing receipt. The consumer's eventual publication and projection use the same stable observation identity for reconciliation.
4. Compare the custody ledger with the component, trust and lifecycle views. Only the source can declare local custody. Only the remote owner can confirm its durable receipt. Only the equipment authority can authorize a physical intervention.

The [evaluation and disposition](../03-evaluate/evidence-and-disposition.md) shows which of these promises can be supported by calculation and which require observation.

[Architecture field guide](../../../README.md)
