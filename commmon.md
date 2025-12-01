# UnmappedDRV spec

## term
UDRV is an abreviation for UnmappedDRV

a UDRV environement is an implementation of the UDRV environement spec

## devices
A udrv_device_t can represent any type of devices such as a keyboard or a bus all device impl must reguster a udrv_device_typedef_t that define fonction for the device
- check : to check if a specific bus addr can be this type of device
- init  : to init a device of this type found on the bus
- destroy : to destroy the device
- ioctl

device also might have an address (udrv_bus_addr_t addr) or not (just NULL) in the later case, they dong belong to any bus and the driver have to implement hotunplug itself

## bus
Bus are a special type of device, they are basicly a list of udrv_bus_addr_t

> [!NOTE]
> about root buses  
> root buses are any bus which their addr is NULL this mean that they don't belong to any bus
