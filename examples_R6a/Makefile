
CC=gcc
CFLAGS=-g -Wall $(LEBOOK_CFLAGS)

EXAMPLE_BINARIES=R6a_ssl_server

all: examples

examples: $(EXAMPLE_BINARIES)

R6a_ssl_server: R6a_ssl_server.o
	$(CC) $(CFLAGS) R6a_ssl_server.o -o R6a_ssl_server -levent -levent_openssl -lssl -lcrypto

.c.o:
	$(CC) $(CFLAGS) -c $<

clean:
	rm -f *~
	rm -f *.o
	rm -f $(EXAMPLE_BINARIES)
