#--
# 
# Copyright (c) 2019-2021 NVIDIA CORPORATION & AFFILIATES. All rights reserved.
# 
# This software is available to you under a choice of one of two
# licenses.  You may choose to be licensed under the terms of the GNU
# General Public License (GPL) Version 2, available from the file
# COPYING in the main directory of this source tree, or the
# OpenIB.org BSD license below:
# 
#     Redistribution and use in source and binary forms, with or
#     without modification, are permitted provided that the following
#     conditions are met:
# 
#      - Redistributions of source code must retain the above
#        copyright notice, this list of conditions and the following
#        disclaimer.
# 
#      - Redistributions in binary form must reproduce the above
#        copyright notice, this list of conditions and the following
#        disclaimer in the documentation and/or other materials
#        provided with the distribution.
# 
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
# EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
# MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
# NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS
# BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN
# ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
# CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
# SOFTWARE.

#--

# Makefile.am -- Process this file with automake to produce Makefile.in

COMMON_DIR = $(top_srcdir)/common
MTCR_DIR = $(top_srcdir)/${MTCR_CONF_DIR}
MTCR_INC_DIR = $(top_srcdir)/include/mtcr_ul
UTILS_DIR = $(top_srcdir)/mft_utils
MLXREG_DIR = $(top_srcdir)/mlxreg

INCLUDES = -I. -I$(USER_DIR) -I$(MTCR_DIR) -I$(MFT_EXT_LIBS_INC_DIR) -I$(UTILS_DIR) -I$(MLXREG_DIR) -I$(MTCR_INC_DIR) $(JSON_CFLAGS)

AM_CFLAGS = -Wall -W -g -MP -MD -pipe  -std=c++11 $(COMPILER_FPIC) -DDATA_PATH=\"$(pkgdatadir)\"

lib_LTLIBRARIES = libprint_util_lib.a

libprint_util_lib_a_SOURCES = mlxlink_cmd_print.h \
                            mlxlink_cmd_print.cpp \
                            mlxlink_record.h \
                            mlxlink_record.cpp
libprint_util_lib_a_LIBDADD = $(JSON_LIBS)
libprint_util_lib_a_CFLAGS = $(AM_CFLAGS)
