# Mac Map 

## Mininet topology:

sudo mn --controller=remote,ip=localhost --topo tree,2


## List Virtual Tenant Network

curl --user "admin":"admin" -H "Content-type: application/json" -X GET http://localhost:8181/restconf/operational/vtn:vtns/

## Create Virtual Tenant Network

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn:update-vtn -d '@vtn1.json'

## Create Virtual Bridge

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn-vbridge:update-vbridge -d '@vbridge1.json'


## Configure Mac Mappings

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn-mac-map:set-mac-map -d '@macmap1.json'


## Delete Virtual Tenant Network

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn:remove-vtn -d '@vtn1.json'




## References:

https://docs.opendaylight.org/en/stable-fluorine/user-guide/virtual-tenant-network-(vtn).html#how-to-create-mac-map-in-vtn


