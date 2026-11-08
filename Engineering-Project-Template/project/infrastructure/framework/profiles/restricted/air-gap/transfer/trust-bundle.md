# Maintain and recover an air-gapped installation

## Goal

A disconnected operator can bootstrap, update and recover a site from vetted local material. Establish what can cross the boundary, who may transfer it, and which evidence must return through the approved channel.

1. Create a dependency closure for one clean host. Include boot image, drivers, firmware compatibility, modules, packages, manifests, verification keys, configuration, licenses, time source and operator instructions. Identify components that silently assume online activation or certificate-status access.
2. Define a transfer manifest with release ID, digest for every item, trust root version, authorized source, permitted target and validity interval. Authenticate the manifest through a separately established trust path. Verify it at both export and intake. Define how operators receive withdrawal notices and replace trust roots when external connectivity is unavailable.
3. Use an intake station and a representative test target according to site policy. Quarantine unexpected media or mismatching bytes. Stage a bounded rollout, preserve the previous compatible media set and record installed revisions by physical asset.
4. Encode the exception process for a critical update between normal transfer windows. Name the risk owner and the point at which the old release must be isolated or retired. Budget spares for transfer media, hardware and licensing devices that are unique to the site.

## Acceptance exercise

Start a spare host with empty caches and no outside route. Install and verify the released set. Alter one file on test media and prove intake rejects it. Recover from an interrupted update using the retained set, then export a redacted installation record through the permitted path. Record any dependency that had to be supplied manually.
