# LEGO Spike Hub and the Motors

A Python snippet utilizing the LEGO Spike motors, [MicroPython](https://lego.github.io/MINDSTORMS-Robot-Inventor-hub-API/), and a variety of commands: `start()`, `stop()`, `run_for_seconds()`, and `run_for_rotations()`.

## Sample Code

```py
from mindstorms import MSHub, Motor, MotorPair
from mindstorms.control import wait_for_seconds
import math

hub = MSHub()

motor_a = Motor('A')
motor_b = Motor('B')

motor_a.run_for_rotations(1, 100)

motor_b.run_for_rotations(1, 10)

motor_a.run_for_seconds(2, 100)

motor_b.run_for_seconds(2, -10)

motor_a.start(100)
motor_b.start(100)

wait_for_seconds(2)

hub.light_matrix.write(motor_a.get_speed())

motor_a.stop()
motor_b.stop()

hub.speaker.beep()
```

***

## Repo Resources

* [Visual Studio Code](https://code.visualstudio.com/)
* [MicroPython for LEGO Robot Inventor](https://www.lego.com/en-ca/themes/mindstorms/downloads)
* [LEGO Mindstorms](https://www.lego.com/en-ca/themes/mindstorms)
* [LEGO Mindstorms App for Mac](https://apps.apple.com/us/app/lego-mindstorms-inventor/id1515448947)
* [LEGO Mindstorms App for Android](https://play.google.com/store/apps/details?id=com.lego.retail.mindstorms)
* [LEGO Mindstorms App for Windows](https://www.microsoft.com/store/apps/9N7GN3KC2GK6)

<a href="https://codeadam.ca">
<img src="https://codeadam.ca/images/code-block.png" width="100">
</a>
