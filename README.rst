!!!! DO NOT USE YET !!!!
========================

esp-idf-ds3231
==============

An esp-idf component for the Analog Devices (Maxim Integrated) DS3231
RTC chip/module.

This my first fully documented and shared open source project. I welcome
comments, suggestions and corrections.

.. figure:: docs/circuit_image.png
   :alt: Cirkit Designwe image of an ESP32 connect to a DS3231 module.

   Cirkit Designwe image of an ESP32 connect to a DS3231 module.

Getting Started
---------------

In and ESP-IDF terminal run:
``idf.py add-dependency "jschwefel/esp-idf-ds3231^1.0.0"`` ###
Prerequisites

The things you need before installing the software.

-  esp-idf v5.0+

Usage
-----

A few examples of useful commands and/or tasks.

::

   i2c_master_dev_handle_t* rtc_handle = ds3231_init_full(GPIO_NUM_2, GPIO_NUM_13);
   char strftime_buf[64];
   struct tm* current_time = ds3231_time_get(rtc_handle);
   strftime(strftime_buf, sizeof(strftime_buf), "%c", current_time);
   printf("The current date/time from the DS3231 is: %s", strftime_buf);
