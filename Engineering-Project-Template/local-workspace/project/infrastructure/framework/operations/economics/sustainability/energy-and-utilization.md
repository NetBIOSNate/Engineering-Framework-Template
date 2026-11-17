# Energy and hardware lifecycle at a useful-work boundary

## Goal

Compare options using energy and materials consumed for a delivered infrastructure outcome. Preserve the service objective, workload mix, recovery capacity and measurement boundary so that the comparison is interpretable.

1. Choose a functional unit, such as 1,000 completed batch jobs at a specified deadline. Record gross energy at the available meter or provider estimate, time interval, utilization, site and what the measurement includes. Separate direct observations from estimates and state uncertainty.
2. At a facility, align IT equipment energy and total facility energy over the same boundary and period when calculating power usage effectiveness (PUE). PUE equals total facility energy divided by IT equipment energy. This ratio cannot identify whether the server is doing useful work. Track both energy per completed job and job completion rate.
3. A test cluster using 240 kWh for 4,000 completed jobs uses 0.06 kWh/job at that measurement boundary. If a denser schedule increases cooling or extends queue time past the deadline, include the new measured effects before adopting it. For carbon estimates, name the source, location and interval for the electricity factor.
4. Consider repair, second use, spare strategy, procurement lead time and support horizon. Replacing hardware shifts material and embodied impacts as well as energy use. Include available supplier evidence and identify gaps.

## Acceptance

Compare several representative periods, including idle and peak operation. Check achieved latency or deadlines and retained failover headroom alongside energy. Record the owner of an actionable decision such as retiring abandoned resources, increasing utilization or adjusting flexible job timing within its deadline.
