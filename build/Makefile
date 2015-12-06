.DEFAULT: build/wedanator

-include *.d

VPATH = ../src

LDFLAGS =

SRCS = $(notdir $(wildcard ../src/*.cc))
OBJS = $(SRCS:%.cc=%.o)

%.o : %.cc
	$(CXX) -c -MMD $< `wx-config --cxxflags` -o $@

wedanator : $(OBJS)
	$(CXX) $(LDFLAGS) $^ `wx-config --libs` -o $@

clean:
	$(RM) $(OBJS) wedanator *.d
