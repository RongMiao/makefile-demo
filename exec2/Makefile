target:= helloworld
all: $(target)

subsystem:= foo smile hello
objs:= $(join $(addsuffix /,$(subsystem)),$(addsuffix .o,$(subsystem)))

CFLAGS:= -w

$(objs):
	cd $(dir $@);$(MAKE)

$(target): $(objs)
	$(CC) $(CFLAGS) $^ -o $@

.PHONY: clean $(subsystem) all
clean:
	-rm $(objs) $(target)