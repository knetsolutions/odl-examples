# Provision L2 Network


## Mininet topology:

sudo mn --controller=remote,ip=localhost --topo tree,2


## List Virtual Tenant Network

curl --user "admin":"admin" -H "Content-type: application/json" -X GET http://localhost:8181/restconf/operational/vtn:vtns/

## Create Virtual Tenant Network

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn:update-vtn -d '@vtn1.json'

## Create Virtual Bridge

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn-vbridge:update-vbridge -d '@vbridge1.json'

## Create Virtual Interface

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn-vinterface:update-vinterface -d '@vif1.json'

## Associate the Physical Port to the Virtual Interface (Port Mapping)

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn-port-map:set-port-map -d '@portmap1.json'


## Get Data flow operaions:

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http:
//localhost:8181/restconf/operations/vtn-flow:get-data-flow -d '@dataflow.json'


## Delete Virtual Tenant Network

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn:remove-vtn -d '@vtn1.json'



## Reference:

https://docs.opendaylight.org/en/stable-fluorine/user-guide/virtual-tenant-network-(vtn).html#how-to-provision-virtual-l2-network
