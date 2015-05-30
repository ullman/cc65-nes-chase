CC65_NESLIB = $(HOME)/cc65/lib/nes.lib 
all: Chase.nes

clean:
	@rm -fv game.o
	@rm -fv Chase.nes
	@rm -fv crt0.o

crt0.o: crt0.s
	ca65 crt0.s

%.o: %.c
	cc65 -Oi $< --add-source
	ca65 $*.s
	rm $*.s

Chase.nes: game.o crt0.o
	ld65 -t nes -o $@ crt0.o $< $(CC65_NESLIB)

.PHONY: clean all

