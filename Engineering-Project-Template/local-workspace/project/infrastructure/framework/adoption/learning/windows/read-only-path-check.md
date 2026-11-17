# Trace a Windows client connection from name to service

## Goal

Practice collecting enough evidence to distinguish a naming failure, a transport failure and an authorization or application failure. Use a hostname and port supplied by the owner of a service you are authorized to test. These native Windows PowerShell examples inspect the client and make a bounded test connection.

```powershell
$serviceName = Read-Host 'Approved service hostname'
[int]$servicePort = Read-Host 'Approved TCP service port'
Get-NetIPConfiguration
Get-DnsClientServerAddress
Resolve-DnsName -Name $serviceName -Type A
Resolve-DnsName -Name $serviceName -Type AAAA
Test-NetConnection -ComputerName $serviceName -Port $servicePort -InformationLevel Detailed
```

1. Record which network interface, resolver, source address, remote address and time were used. A roaming laptop may use a different route or resolver while connected to a VPN. Store diagnostic output according to its sensitivity.
2. Compare returned addresses with the service owner's expected answers. An absent AAAA record can be expected for an IPv4-only service. For a dual-stack service, test each expected IP individually with the same TCP port. Record which address family succeeded. An IP-only TCP check does not validate hostname-based TLS or service authorization.
3. Complete one documented service operation using the legitimate client identity and normal service name. Record the safely shareable status and the corresponding service-side event. An open port alone cannot demonstrate a valid certificate, a trusted issuer or correct read permissions.
4. Repeat from another approved client segment if the expected behavior differs there. For a denial test, identify the policy that should deny access. A name-resolution error cannot establish that the intended firewall rule blocked the flow.

## Deliverable

Provide a short timeline identifying the last successful layer, first failure and next owner. Use the [dependency register](../../../records/design/interfaces/dependency-register.md) to record a repeatable test and its expected result.
