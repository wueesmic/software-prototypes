# Simple Makefile
src = $(wildcard *.c)
# $(wildcard ../libs/*.c)
obj = $(src:.c=.o)
dep = $(obj:.o=.d)  # one dependency file for each source

TARGET = dma-proxy-test

# CFLAGS =  -D_FILE_OFFSET_BITS=64 -D_GNU_SOURCE -D_LARGE_FILE_SOURCE
# CFLAGS =  -D_FILE_OFFSET_BITS=64 -D_GNU_SOURCE -D_LARGE_FILE_SOURCE
CFLAGS = -I../Common
LFLAGS = -pthread

$(TARGET): $(obj)
        echo $(src)
        $(CC) $(CFLAGS) $(LFLAGS) -o $@ $^

%.o: %.c
        $(CC)  $(CFLAGS) -c -o $@ $<

.PHONY : clean
clean:
        rm -f  $(obj) $(TARGET)

