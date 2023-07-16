dir:= $(shell pwd)
obj:= $(addsuffix .o,$(notdir $(dir)))
CFLAGS:= -I ../include
all:$(obj)

$(obj): %.o: %.c
	gcc $(CFLAGS) -c $^ -o $@

.PHONY: clean all
clean:
	-rm *.o hello