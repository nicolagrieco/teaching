CFLAGS = -DDEBUG
CFLAGS = -g
LDFLAGS = -L/usr/lib/i386-linux-gnu/ -lssl -lcrypto 
OBJ=funcManagement.o main.o gateFunct.o encode.o decode.o ecbaes.o select.o loadGarb.o


main: ${OBJ}
	gcc -o main ${OBJ} -lssl -lcrypto  

mainecb: ecbaes.o mainecb.o
	gcc -o mainecb mainecb.o ecbaes.o -lssl -lcrypto  

aes: aes.o
	gcc -o aes aes.o -lssl -lcrypto  

clean: 
	rm -f main ${OBJ}
	rm -f aes aes.o
	rm -f mainecb mainecb.o ecbaes.o

