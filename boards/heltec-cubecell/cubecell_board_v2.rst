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

.. _board_heltec-cubecell_cubecell_board_v2:

Heltec CubeCell-Board-V2 (HTCC-AB01-V2)
=======================================

.. contents::

Hardware
--------

Platform :ref:`platform_heltec-cubecell`: Heltec CubeCell is an easy-to-use LoRa Node series brand based on a highly integrated and ultra low power SoC and the LoRa SX1262 transceiver.

.. list-table::

  * - **Microcontroller**
    - ASR6501
  * - **Frequency**
    - 48MHz
  * - **Flash**
    - 128KB
  * - **RAM**
    - 16KB
  * - **Vendor**
    - `Heltec <https://heltec.org/project/htcc-ab01-v2/?utm_source=platformio.org&utm_medium=docs>`__


Configuration
-------------

Please use ``cubecell_board_v2`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:cubecell_board_v2]
  platform = heltec-cubecell
  board = cubecell_board_v2

You can override default Heltec CubeCell-Board-V2 (HTCC-AB01-V2) settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `cubecell_board_v2.json <https://github.com/HelTecAutomation/platform-heltec-cubecell/blob/master/boards/cubecell_board_v2.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:cubecell_board_v2]
  platform = heltec-cubecell
  board = cubecell_board_v2

  ; change microcontroller
  board_build.mcu = asr6501

  ; change MCU frequency
  board_build.f_cpu = 48000000L

Debugging
---------
:ref:`piodebug` currently does not support Heltec CubeCell-Board-V2 (HTCC-AB01-V2) board.

Frameworks
----------
.. list-table::
    :header-rows:  1

    * - Name
      - Description

    * - :ref:`framework_arduino`
      - Arduino Wiring-based Framework allows writing cross-platform software to control devices attached to a wide range of Arduino boards to create all kinds of creative coding, interactive objects, spaces or physical experiences