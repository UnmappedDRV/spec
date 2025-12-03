# Unmapped DRV spec

## functions
All UDRV environements must implements a set of functions

## mandatory
void log (int level, const char \*fmt, va_list args)
void \*malloc(size_t size)
void free(void \*ptr)

## optional

## module loading
The process of loading a driver is done by loading a ELF relocatble file and link it with the udrv environement runtime
