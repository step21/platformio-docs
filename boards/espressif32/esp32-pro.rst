..  Copyright (c) 2014-present PlatformIO <contact@platformio.org>
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
       http://www.apache.org/licenses/LICENSE-2.0
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

.. _board_espressif32_esp32-pro:

OLIMEX ESP32-PRO
================

.. contents::

Hardware
--------

Platform :ref:`platform_espressif32`: ESP32 is a series of low-cost, low-power system on a chip microcontrollers with integrated Wi-Fi and Bluetooth. ESP32 integrates an antenna switch, RF balun, power amplifier, low-noise receive amplifier, filters, and power management modules.

.. list-table::

  * - **Microcontroller**
    - ESP32
  * - **Frequency**
    - 240MHz
  * - **Flash**
    - 4MB
  * - **RAM**
    - 320KB
  * - **Vendor**
    - `OLIMEX <https://www.olimex.com/Products/IoT/ESP32/ESP32-PRO/open-source-hardware?utm_source=platformio.org&utm_medium=docs>`__


Configuration
-------------

Please use ``esp32-pro`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:esp32-pro]
  platform = espressif32
  board = esp32-pro

You can override default OLIMEX ESP32-PRO settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `esp32-pro.json <https://github.com/platformio/platform-espressif32/blob/master/boards/esp32-pro.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:esp32-pro]
  platform = espressif32
  board = esp32-pro

  ; change microcontroller
  board_build.mcu = esp32

  ; change MCU frequency
  board_build.f_cpu = 240000000L


Uploading
---------
OLIMEX ESP32-PRO supports the following uploading protocols:

* ``espota``
* ``esptool``

Default protocol is ``esptool``

You can change upload protocol using :ref:`projectconf_upload_protocol` option:

.. code-block:: ini

  [env:esp32-pro]
  platform = espressif32
  board = esp32-pro

  upload_protocol = esptool

Debugging
---------
:ref:`piodebug` currently does not support OLIMEX ESP32-PRO board.

Frameworks
----------
.. list-table::
    :header-rows:  1

    * - Name
      - Description

    * - :ref:`framework_arduino`
      - Arduino Wiring-based Framework allows writing cross-platform software to control devices attached to a wide range of Arduino boards to create all kinds of creative coding, interactive objects, spaces or physical experiences

    * - :ref:`framework_espidf`
      - ESP-IDF is the official development framework for the ESP32 and ESP32-S Series SoCs.