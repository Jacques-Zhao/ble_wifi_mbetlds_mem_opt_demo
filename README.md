| Supported Targets | ESP32 | ESP32-C2 | ESP32-C3 | ESP32-C6 | ESP32-S3 |
| ----------------- | ----- | -------- | -------- | -------- | -------- |

# BLE Peripheral with HTTPS connection

(See the README.md file in the upper level 'examples' directory for more information about examples.)

This example aims to run https connect (auto light sleep mode) along with BLE GATT server simultaneously using NimBLE host stack. It is a combination of 3 examples in IDF: `bluetooth/nimble/bleprph`, `wifi/power_save` and `protocols/https_mbedtls`. See the README.md files of these examples to know more about them.

### BLE peripheral

This example creates GATT server and then starts advertising, waiting to be connected to a GATT client.

It uses ESP32's Bluetooth controller and NimBLE stack based BLE host.

### https

Simple HTTPS request example that uses mbedTLS to establish a secure socket connection using the certificate bundle with two custom certificates added for verification:

## How to Use Example

Before project configuration and build, be sure to set the correct chip target using:

```bash
idf.py set-target esp32c3 or idf.py set-target esp32c2
```

### Configure the project

Open the project configuration menu: 

```bash
idf.py menuconfig
```

In the `Example Configuration` menu:

* Enter SSID and password of known Wi-Fi AP with connectivity to internet.

## Testing

To test this demo, any BLE scanner app and a WiFi access point with internet connectivity can be used.

### Build and Flash

Run `idf.py -p PORT flash monitor` to build, flash and monitor the project.

(To exit the serial monitor, type ``Ctrl-]``.)

See the [Getting Started Guide](https://idf.espressif.com/) for full steps to configure and use ESP-IDF to build projects.
