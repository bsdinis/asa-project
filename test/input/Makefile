CC := g++
VPATH := .:../../network
INCLUDES := -I. -I../../network
CXXFLAGS := -Wall -Werror -g -fdiagnostics-color=always $(INCLUDES)
LDFLAGS := -Wall -Werror -fdiagnostics-color=always $(INCLUDES) -L. -L../../graph -L../../network

SOURCES=$(wildcard *.cpp) network.cpp
OBJECTS=$(SOURCES:.cpp=.o)
TARGET =input_test


all: $(TARGET)

$(TARGET): $(OBJECTS)

.PHONY: clean
clean:
	rm -f $(OBJECTS) $(TARGET) vgcore*

.PHONY: depend
depend: $(SOURCES)
	$(CC) $(INCLUDES) -MM $(SOURCES) > autodep
	@echo $(SOURCES)
