## Labgrid playground

### Client to Exporter communication
> Labgrid requires your user to be able to connect from the client machine via ssh to the exporter machine _without_ a password prompt. This means that public key authentication should be configured on all involved machines for your user beforehand.


### Resource allocation

#### Reservation
"First come, first served" reservation of resources with a mandatory expiration.

#### Locking
While a resource is allocated for a reservation, only the owner of the reservation can lock that place. Other resources can be locked by anyone. Resources wouldn't be automatically freed when clients leave, but others can kick them out.

### Authentication
No authentication is supported at this time: https://github.com/labgrid-project/labgrid/blob/9e0562e1c8d6842c850c239d64896b88c3bf3bd1/labgrid/remote/coordinator.py#L139
