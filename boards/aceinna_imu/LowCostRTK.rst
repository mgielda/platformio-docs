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

.. _board_aceinna_imu_LowCostRTK:

Aceinna Low Cost RTK
====================

.. contents::

Hardware
--------

Platform :ref:`platform_aceinna_imu`: Open-source, embedded development platform for Aceinna IMU hardware. Run custom algorithms and navigation code on Aceinna IMU/INS hardware.

.. list-table::

  * - **Microcontroller**
    - STM32F469NIH6
  * - **Frequency**
    - 180MHz
  * - **Flash**
    - 1MB
  * - **RAM**
    - 384KB
  * - **Vendor**
    - `Aceinna <https://www.aceinna.com/inertial-systems/?utm_source=platformio&utm_medium=docs>`__


Configuration
-------------

Please use ``LowCostRTK`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:LowCostRTK]
  platform = aceinna_imu
  board = LowCostRTK

You can override default Aceinna Low Cost RTK settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `LowCostRTK.json <https://github.com/aceinna/platform-aceinna_imu/blob/master/boards/LowCostRTK.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:LowCostRTK]
  platform = aceinna_imu
  board = LowCostRTK

  ; change microcontroller
  board_build.mcu = stm32f469nih6

  ; change MCU frequency
  board_build.f_cpu = 180000000L


Uploading
---------
Aceinna Low Cost RTK supports the next uploading protocols:

* ``blackmagic``
* ``jlink``
* ``stlink``

Default protocol is ``stlink``

You can change upload protocol using :ref:`projectconf_upload_protocol` option:

.. code-block:: ini

  [env:LowCostRTK]
  platform = aceinna_imu
  board = LowCostRTK

  upload_protocol = stlink

Debugging
---------

:ref:`piodebug` - "1-click" solution for debugging with a zero configuration.

.. warning::
    You will need to install debug tool drivers depending on your system.
    Please click on compatible debug tool below for the further
    instructions and configuration information.

You can switch between debugging :ref:`debugging_tools` using
:ref:`projectconf_debug_tool` option in :ref:`projectconf`.

Aceinna Low Cost RTK has on-board debug probe and **IS READY** for debugging. You don't need to use/buy external debug probe.

.. list-table::
  :header-rows:  1

  * - Compatible Tools
    - On-board
    - Default
  * - :ref:`debugging_tool_blackmagic`
    - 
    - 
  * - :ref:`debugging_tool_jlink`
    - 
    - 
  * - :ref:`debugging_tool_stlink`
    - Yes
    - Yes