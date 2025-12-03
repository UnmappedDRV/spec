# Unmapped DRV spec

## format
All drivers must be relocatbles ELF files

## entry point and metadata
All driver can must have have a metadata global struct called udrv_meta (udrv_driver_t udrv_meta) they can define an init function and fini function in it along name and others things

## io
For io devices (on x86) have access to port io via function and MUST never use port io direcly via inline assembly
- void udrv_out_byte(udrv_port_t port, uint8_t data);
- uint8_t udrv_in_byte(udrv_port_t port);
- void udrv_out_word(udrv_port_t port, uint16_t data);
- uint16_t udrv_in_word(udrv_port_t port);
- void udrv_out_dword(udrv_port_t port, uint32_t data);
- uint32_t udrv_in_dword(udrv_port_t port);

> [!NOTE]
> prototype for these functions can be found in the sdk in include/udrv/io.h

> [!NOTE]
> result of these function on arch other than x86 is undefined
