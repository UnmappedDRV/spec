# Unmapped DRV spec

## functions
All UDRV environements must implements a set of functions

## mandatory
void log (int level, const char \*fmt, va_list args)
void \*malloc(size_t size)
void free(void \*ptr)

## optional

## module loading
To load a module the module loader must load a ELF relocatble file and call a function called udrv_entry (int udrv_entry(udrv_env_t \*env, int argc, const char \*argv)) if the entry point return a negative value the module musy be unloaded
