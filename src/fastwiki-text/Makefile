root = ..
include $(root)/rules.mk

objs = $(patsubst %.cpp,%.o, $(wildcard *.cpp))

program = fastwiki-text$(file_type)

%.o:%.cpp
	@$(cpp) $(cppflag) $(inc) -o $@ -c $<
	@echo "  CC    $@"

all: $(program)

$(program): fastwiki-text.o
	$(cpp) -o $@ $^ $(libs)

clean:
	rm -f $(program) $(objs)
