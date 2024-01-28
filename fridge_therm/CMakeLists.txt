#
# Copyright (C) 2024 Jamie M.
#
# SPDX-License-Identifier: Apache-2.0
#

cmake_minimum_required(VERSION 3.20.0)

if(NOT SYSBUILD)
  message(FATAL_ERROR "This project requires sysbuild")
endif()

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(fridge_therm)

target_sources(app PRIVATE src/main.c)
