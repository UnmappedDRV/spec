# Unmapped DRV spec

## format
All drivers must be relocatbles ELF files

## entry point and metadata
All driver can must have have a metadata global struct called udrv_meta (udrv_driver_t udrv_meta) they can define an init function and fini function in it along name and others things
