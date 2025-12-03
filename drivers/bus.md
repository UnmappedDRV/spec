# Unmapped DRV spec

## bus
Bus are a special type of devices thag contain a list of bus address. Each bus address represent an address on the bus. Bus addresses have a generic struct (udrv_bus_addr_t) and a bus specific extention (udrv_pci_addr_t). The bus extention give more bus specific information such has DeviceID/VendorID on pci

> [!NOTE]
> one can use udrv_bus_addr_t->type to check the bus specific extention to use
