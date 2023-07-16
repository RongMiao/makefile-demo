D_SRC:= ./src
srcs:= $(wildcard $(D_SRC)/*.c)
objs:= $(patsubst %.c,%.o,$(srcs))

CFLAGS := -I include

all: hello 

$(objs):%.o: %.c
	gcc $(CFLAGS) -c $^ -o $@

%.o: %.c
	gcc -c $^ -o $@

hello: $(objs) rainny.o
	gcc $^ -o $@
		
.PHONY: clean all
clean:
	-rm $(objs) *.o hello