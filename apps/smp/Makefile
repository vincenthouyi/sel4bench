#
# Copyright 2017, Data61
# Commonwealth Scientific and Industrial Research Organisation (CSIRO)
# ABN 41 687 119 230.
#
# This software may be distributed and modified according to the terms of
# the BSD 2-Clause license. Note that NO WARRANTY is provided.
# See "LICENSE_BSD2.txt" for details.
#
# @TAG(DATA61_BSD)
#

# Targets
TARGETS := $(notdir $(SOURCE_DIR)).bin

# Make sure this symbol stays around as we don't reference this, but
# whoever loads us will
LDFLAGS += -u __vsyscall_ptr

# Source files required to build the target
CFILES :=  $(sort $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/src/*.c)))

# Libraries
LIBS := sel4 c cpio sel4muslcsys utils sel4utils sel4allocman elf sel4vspace sel4simple sel4vka\
	    sel4bench sel4benchsupport sel4debug platsupport sel4platsupport sel4simple-default sel4serialserver

include $(SEL4_COMMON)/common.mk
