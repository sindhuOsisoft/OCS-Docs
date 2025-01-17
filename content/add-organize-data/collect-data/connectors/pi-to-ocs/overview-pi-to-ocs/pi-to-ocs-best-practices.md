---
uid: bpPISystemConnection
---

# PI System connections best practices

Only one PI to OCS Agent per connection is allowed to transfer data from a specific PI Data Archive and an optional AF server to a namespace. This restriction prevents multiple PI to OCS Agents from pulling data from a single PI Data Archive, which can create an excessive load on the server. The following actions are recommended to address this issue:

- Install the PI to OCS Agent on a host computer that is separate from the PI Data Archive deployment, so it does not add to the load on the server.

- Keep the PI to OCS Agent software version up-to-date for the best performance. The portal indicates when an agent is out of date and needs to be updated. 
