# I2C MPU6050 ESP-IDF Example 

## Overview

This example is based onthe I2C_simple example from the examples/peripherals/i2c folder on ESP_IDF. It shows the accelerometer and gyroscope outputs on each axys(x,y,z).

The next version will be able to calibrate and specify the output precision.

***This documentation is also based on the i2c_simple example from ESP_IDF***
## How to use example

### Hardware Required

To run this example, you need a ESP32, a MPU6050 and jumpers for connection.The MPU6050 contains an accelerometer, gyroscope and can only use I2C for communication.

#### Pin Assignment:

**Note:** The following pin assignments are used by default, you can change these in the `menuconfig` .

|                  | SDA             | SCL           |
| ---------------- | -------------- | -------------- |
| ESP I2C Master   | I2C_MASTER_SDA | I2C_MASTER_SCL |
| MPU9250 Sensor   | 21             | 22            |


The pins are directly defined in the code but this values can be replaced by Ì2C_MASTER_SDA and I2C_MASTER_SCL`  in order to use the PINS defined in Example configuration in **idf.py menuconfig**

**Note:** There's no need to add an external pull-up resistors for SDA/SCL pin, because the driver will enable the internal pull-up resistors.

### Build and Flash

Enter `idf.py -p PORT flash monitor` to build, flash and monitor the project.

(To exit the serial monitor, type ``Ctrl-]``.)

See the [Getting Started Guide](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/index.html) for full steps to configure and use ESP-IDF to build projects.

## Example Output

```bash
I (328) MPU6050: I2C initialized successfully
I (338) MPU6050: QUIEN_SOY = 68
I (338) MPU6050: ACCE X=0.0 Y=0.0 Z=0.0
I (338) MPU6050: GYRO X=0..0 Y=0.0 Z=0.0


I (338) i2c-simple-example: I2C de-initialized successfully
```
