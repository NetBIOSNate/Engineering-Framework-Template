# Field observations, part 3 — evidence and disposition

The decision under review is ADR-01, durable device capture. This is an illustrative design review. The numerical entries below are calculations, and no real device test results are claimed.

## CAP-01 — storage and recovery assumptions

Twelve hours at two observations/s produces 12 × 3,600 × 2 = 86,400 observations. At 600 payload bytes each, the minimum payload storage is 51,840,000 bytes. A planning factor of 1.5 gives 77,760,000 bytes. Measure formatted capacity, journal overhead, write amplification, reserve and degradation over service life before selecting hardware.

With 10 confirmed observations/s after reconnect and two/s of ongoing live traffic, net service is eight/s. Ideal drain time is 86,400 / 8 = 10,800 seconds, or three hours. To finish in strictly less than four hours at this arrival rate requires **more than eight confirmed observations/s total**. Exactly eight/s gives six/s net and exactly four hours, before startup or overhead. The model has positive margin at ten/s. It does not establish field throughput.

## Trace and evidence plan

| Driver or risk | Decision and mechanism | Evidence and proposed criterion | State and owner |
| --- | --- | --- | --- |
| QS-01 | ADR-01, journal before local receipt | VER-01 cuts power around commit and acknowledgment. Recover every locally acknowledged ID | Planned, device lead |
| QS-02 | IF-01 and IF-02, deduplicated durable intake with verified receipt | VER-02 repeats upload after lost receipt. Observe one canonical record and one eventual effect per accepted ID | Planned, platform lead |
| QS-02 | CAP-01, service reserve during recovery | VER-03 preloads the outage cohort, keeps live arrival at two/s and times drain to complete reconciliation in less than four hours | Calculated estimate, service lead owns measurement |
| QS-03 | CTX-01, separate capture and receipt time and expose uncertainty | VAL-01 asks an operator to distinguish an old reading from a current one after a clock reset | Planned intended-use exercise, operator lead |
| RSK-01 | Reserved space and controlled refusal when capacity is exhausted | VER-04 fills storage and checks the inspector sees a refusal before custody transfers | Planned, field-product lead |

## Review disposition

Proceed to a representative device trial. Keep procurement open until power-loss, usable-capacity, endurance and drain evidence is available. If the measured rate is eight/s or lower, QS-02 cannot meet the strict target under this model. Reopen capacity, scheduling or the agreed recovery target. If an acknowledged ID is lost, reopen the receipt contract and persistence design.

The sponsor still owns the decision about physical loss of the only offline device. A passing restart test cannot close that risk. Record any decision to accept it with the affected scope and review trigger. Use the [evidence worksheet](../../../worksheets/assurance/scenario-and-review.md) to capture real observations on a project.

[Architecture field guide](../../../README.md)
