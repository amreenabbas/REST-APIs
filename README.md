Service API - The service API deals with the physical resources and services in the smart city. For e.g. an application may need to use resources like Variable Messaging Systems (VMS), Public Announcement Systems and etc. that have been deployed. 
              The service APIs allow the authorized user to search for available service and retrieve information about supported API’s to avail the offered service by that resource, as meta information. The meta information thus retrieved helps the user to:

  <ul><li>Discover requisite authorization procedure to access the service 
  <li>Reserve the service, if required
  <li>Modify the reservation
  <li>Tear down the reservation
  <li>Access (read/write) the resources with authorization as applicable
  <li>Get status of offered service

The APIs are written in Flask, a micro webframework written in Python and the PostgreSQL database has been used for storage.
The APIs are used by users to sign up, create groups of devices and reserve those groups. After obtaining a reservation-id the user can configure the devices and write content to the devices. These APIs are a reference implementation of the write APIs. The database consists of following tables.

devices - It contains list of devices.
users - It contanis information about the users.
groups - It contains list of groups made by users. 
reservations - It conatins information regarding the reservation time. 
reservations_info - It contains reservation information. 
device_state - It contains information about devices in a reservation. 
configure - It contains the device configurations.
write_op - It contains the device content.
