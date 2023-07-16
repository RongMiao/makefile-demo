dir:= $(shell pwd)
obj:= $(addsuffix .o,$(notdir $(dir)))

all:$(obj)

$(obj): %.o: %.c
	gcc -c $^ -o $@

.PHONY: clean all
clean:
	-rm *.o hello