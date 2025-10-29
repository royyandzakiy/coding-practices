- Enabling to call C header files within C++ files

```c

#ifdef __cplusplus
extern "C" {
#endif

#include "lv_obj.h"
#include "../hal/lv_hal_indev.h"
#include "lv_group.h"

void lv_indev_read_timer_cb(lv_timer_t * timer);
void lv_indev_enable(lv_indev_t * indev, bool en);

#ifdef __cplusplus
}
#endif
```