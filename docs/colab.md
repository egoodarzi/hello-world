```
import tensorflow as tf
from tensorflow.python.client import device_lib

device_name = tf.test.gpu_device_name()
print(device_name)

device_lib.list_local_devices()

!cat /proc/cpuinfo
!cat /proc/meminfo
```
