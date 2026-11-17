# Bare-metal bootstrap and out-of-band recovery

A replacement server should reach a known, supportable state even when its operating system and primary workload network are unavailable. Treat its baseboard management controller (BMC), the embedded management computer, as a privileged control endpoint.

## Commission one host

1. Match asset identifier, chassis serial, switch ports, intended rack and role to the approved build record. Verify target identity before any imaging operation. Separate the BMC network from tenant traffic, restrict administrative access, rotate bootstrap credentials and capture a console-access audit event.
2. Establish power, console, firmware inventory, trusted time and the signed boot path appropriate to the hardware. Pin an approved image and firmware combination. Document the verification key, mirror location, recovery media custodian and procedure for equipment that cannot use network boot.
3. Discover network interfaces and storage by stable identifiers. Select only the approved installation disk. Quarantine an unexpected disk map or serial mismatch for operator review. Verify management reachability before moving the host into its production segment.
4. Enroll the host identity, install monitoring and qualify CPU, memory, storage and network links. Admit the host to scheduling only after its hardware inventory and expected health checks agree.

## Prove replacement

On a spare host, rebuild with an empty local cache. Disable its workload link and use the console path to inspect boot status. Verify tenant credentials cannot access the BMC. Record time to schedule work again, image digest, firmware version and console event. If the image fails, recover through the documented previous image or rescue media. Rotate any temporary access credential when commissioning ends.
