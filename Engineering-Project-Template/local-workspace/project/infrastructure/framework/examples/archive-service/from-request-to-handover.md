# Worked design review for a recoverable archive

This is an illustrative project with invented measurements. It carries one decision from a consumer interview through a launch review. Replace the figures and observations when adopting the design.

## 1. Give the service a consumer and a clock

A survey team publishes immutable daily exports and amends metadata throughout the day. An analyst must retrieve the latest published export by 07:00 local time. After site loss, the team accepts four hours to restore the active 2 TiB archive and at most 15 minutes of lost acknowledged metadata updates. Data loss is measured using a numbered marker in each acknowledged metadata transaction. The 15-minute limit applies to metadata, independent of the nightly export schedule.

## 2. Draw both paths

The producer obtains a scoped identity, writes a versioned object, verifies its digest and publishes a manifest pointing to that version. The reader resolves the service name, authenticates, reads the manifest and verifies the object. The recovery path needs an independent operator identity, historical decryption keys, the manifest history, copied object versions, clean infrastructure definitions, network access and a consumer probe. A recovered manifest referencing an uncopied object is an unusable recovery point.

## 3. Compare two viable recovery tiers

| Candidate | Transfer model | Consequence |
| --- | --- | --- |
| Restore 2 TiB from a cold path at a measured 100 MiB/s | 2,097,152 MiB / 100 / 3,600 = 5.83 h | Transfer exceeds the four-hour limit before retrieval, setup and checks. Suitable if the owner relaxes the objective. |
| Recover from a verified copy with a 200 MiB/s sustained path | 2,097,152 / 200 / 3,600 = 2.91 h | With 15 min to obtain access and provision, 20 min to replay metadata and 15 min to validate, the modeled total is about 3.75 h. |

The second option leaves roughly 15 minutes of margin. Select a separately administered copy only if sustained throughput under load, consistent manifest history and required keys can be demonstrated together. Fund the retained copy and measure effective full-volume recovery. A high watermark or sample restore alone cannot qualify the four-hour claim.

## 4. Assemble and introduce

Use the [assembly guide](../../design/composition/bindings/environment-assembly.md) to bind networking, identity, storage, observability and recovery. Development uses synthetic exports. Testing drops a copy event and verifies the recovery catalog withholds the incomplete manifest. Staging exercises historical keys, cold reads and a denied deletion. In production, begin with one export stream. Advance after its consumer read, digest and replicated manifest are verified. Keep the previous published manifest addressable until reversal ends.

## 5. Rehearse the decision

At 09:00 the exercise controller isolates the primary. The most recent fully consistent recovery marker is 08:51. A new reader verifies the archive at 12:46. Those illustrative observations imply a nine-minute point gap and a 3 h 46 min interruption. The reviewer checks full-volume transfer, metadata integrity, sampling interval and the independent credentials used. Record a hold if even one required object or key is missing.

## 6. Hand over the next decision

The service record names the storage operator, survey acceptance owner, on-call route, restore evidence and approved spend. Re-test when the active archive grows. At 2.5 TiB and the same rate, transfer alone reaches about 3.64 h. Adding the same 50 minutes exceeds four hours. Before accepting that growth, benchmark a faster recovery path or negotiate a different active set and objective.

Copy the [decision record](../../records/design/decision.md), [change packet](../../records/delivery/change-packet.md) and [recovery trial sheet](../../records/assurance/exercises/recovery-trial.md) to carry this pattern into a real project.
