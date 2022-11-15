### 修改
```c
#ifndef __GNU_VISIBLE
#include <dlfcn.h>
#else
typedef struct Dl_info Dl_info;

struct Dl_info
{
    char        dli_fname[PATH_MAX];  /* Filename of defining object */
    void       *dli_fbase;            /* Load address of that object */
    const char *dli_sname;            /* Name of nearest lower symbol */
    void       *dli_saddr;            /* Exact value of nearest symbol */
};

extern int dladdr (const void *addr, Dl_info *info);
#endif
```