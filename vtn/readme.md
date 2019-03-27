# Verification

curl --user "admin":"admin" -H "Content-type: application/json" -X GET http://localhost:8181/restconf/operational/vtn:vtns/

# Create Virtual Tenant Network

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn:update-vtn -d '@vtn1.json'

# Create Virtual Bridge

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn-vbridge:update-vbridge -d '@vbrige1.json'

# Create Virtual Interface

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn-vinterface:update-vinterface -d '@vif1.json'

# Associate the Physical Port to the Virtual Interface (Port Mapping)

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn-port-map:set-port-map -d '@portmap.json'


# Get Data flow operaions:






# Delete Operations

# Delete Virtual Tenant Network

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn:remove-vtn -d '@vtn1.json'




# Router

curl --user "admin":"admin" -H "Content-type: application/json" -X POST http://localhost:8181/restconf/operations/vtn-vrouter:update-vrouter -d '@vrouter1.json'


