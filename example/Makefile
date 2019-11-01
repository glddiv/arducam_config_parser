CROSS_COMPILE 	?=
CC				=$(CROSS_COMPILE)gcc
CFLAGS			= 
LIBS			= -larducam_config_parser

%.o : %.c
	$(CC) $(CFLAGS) -c -o $@ $<
all: toJson toYaml

toJson: toJson.o
	$(CC) $(CFLAGS) $^ -o $@ $(LIBS)

toYaml: toYaml.o
	$(CC) $(CFLAGS) $^ -o $@ $(LIBS)

clean:
	rm -f *.o
	rm -f toJson
	rm -f toYaml