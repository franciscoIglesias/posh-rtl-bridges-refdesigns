# 
# Copyright (c) 2019 Xilinx Inc.
# Written by Alok Mistry.
# 
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
# 
# The above copyright notice and this permission notice shall be included in
# all copies or substantial portions of the Software.
# 
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL
# THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
# THE SOFTWARE.
# 
# Description: 
#   Makefile to generate all designs and ips.
# 

include ./Rules.mk

POSH_REPO = ./..

SUBDIRS += $(HN_F_PCORE_DIR)
SUBDIRS += $(RN_F_PCORE_DIR)
SUBDIRS += ./vivado_designs/chi_ref_design

all: $(SUBDIRS)

.PHONY : $(SUBDIRS)

$(SUBDIRS):
	$(MAKE) -C $@

clean:  $(SUBDIRS:%=%-clean)


$(SUBDIRS:%=%-clean):
	$(MAKE) -C $(@:-clean=) clean


