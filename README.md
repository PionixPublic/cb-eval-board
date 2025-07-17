# ChargeBridge Evaluation Board

This repository contains the KiCad project files for the **ChargeBridge Evaluation Board**, released as open hardware.

> [!NOTE]  
> KiCad version **9.0.2 or newer** is required to open this project. [Download KiCad](https://www.kicad.org/)

![CB Eval Board 3D View](https://github.com/PionixPublic/cb-eval-board/blob/main/cb-eval.png?raw=true)

### Overview

This evaluation board is designed to facilitate testing and development with **Pionix ChargeBridge modules**, supporting **all major charging standards**. It is compatible with both **EVSE (Electric Vehicle Supply Equipment)** and **EV (Electric Vehicle)** ChargeBridge modules.

### Use Cases

* **Dual-Board Evaluation Setup**:
  Using two evaluation boards (one with an EVSE module and one with an EV module), you can create a fully functional desktop test environment where the EV module simulates a vehicle being charged by the EVSE module.

* **Standalone Charger Development**:
  A single board can be integrated into a **fully operational AC or DC charger** by connecting appropriate external components such as:

  * Contactors or relays
  * Isolation monitoring devices
  * DC power supplies
  * Power meters

### Mechanical Mounting

The board can be DIN rail mounted using a suitable adapter, enabling integration into control cabinets or industrial test setups.

For more details refer to the PDF datasheet.

> [!WARNING]  
> This is a pre-release version and has not yet been fully tested. The official release is planned for October 2025.


## Features
============

* **Wide Input Voltage Range**:
  `VSUPPLY` input supports **9–30 V**

* **Charging Cable Interface**:
  7-pin connector supporting **all major charging standards**

* **Temperature Sensing**:

  * 2× **PT1000** sensor inputs
  * **On-board PCB temperature monitoring**

* **Relay Control**:

  * 3× relay drivers for **VSUPPLY** (with **feedback** inputs)

* **High-Voltage Safety Monitoring**:

  * Input for **DC overvoltage shutdown**
  * Compliant with **IEC 61851-23:2023**, sections **6.3.1.106.2** and **6.3.1.106.3**
  * Supports up to **1200 V**

* **Communication Interfaces**:

  * **Ethernet** and **USB-C** for host communication
  * **UART (3.3 V TTL level)**
  * **CAN** with onboard termination
  * **RS485** with onboard termination
  * **Debug UART** pin header compatible with FTDI cables

* **User Interface & Control**:

  * **RGB LED** for charging status indication
  * Push buttons for:

    * Stop charging
    * Emergency stop
    * Module secure
    * Reset
  * **Emergency stop I/O** and **stop charging input** (up to VSUPPLY)

* **General Purpose I/O**:

  * 5× digital inputs
  * 5× digital outputs (all at VSUPPLY level)

* **Power & Measurement**:

  * VSUPPLY voltage monitoring
  * Integrated **shunt resistor** for measuring ChargeBridge current consumption

