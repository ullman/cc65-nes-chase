CC65_NESLIB = $(HOME)/cc65/lib/nes.lib 
all: Chase.nes

clean:
	@rm -fv game.o
	@rm -fv Chase.nes
	@rm -fv crt0.o

Chase.nes: game.c crt0.s
	cl65 -t nes -o $@ game.c crt0.s $(CC65_NESLIB)

.PHONY: clean all

