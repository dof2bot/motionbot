#
# @brief   motionbot-desktop
# @version 1.0.0
# @date    Fri 03 Dec 2021 10:37:52 AM CET
# @company None, free software to use 2021
# @author  Vladimir Roncevic <elektron.ronca@gmail.com>
#

CC=g++
RM=rm

include ccflags.mk
include ldflags.mk
include sources.mk
include objects.mk

EXECUTABLE=motionbot-desktop

all: $(SOURCES) $(EXECUTABLE)

$(EXECUTABLE): $(OBJECTS)
	$(CC) $(LDFLAGS) $(OBJECTS) -o $@ `pkg-config gtkmm-3.0 --libs`

.cc.o:
	$(CC) $(CFLAGS) $< -o $@ `pkg-config gtkmm-3.0 --cflags`

clean:
	$(RM) -rf ../*.o $(EXECUTABLE)
