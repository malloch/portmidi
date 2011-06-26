SRC=../porttime/ptmacosx_cf.c ../pm_common/pmutil.c ../pm_common/portmidi.c ./pmmac.c ./pmmacosxcm.c ./finddefault.c ./readbinaryplist.c
OBJ=$(SRC:.c=.o)
OUT=libportmidi.a
INCLUDES=-I../porttime -I../pm_common -I.
CFLAGS=-O2
GCC=gcc
LDFLAGS=-framework Carbon -framework CoreMidi -framework CoreAudio

default: $(OUT)

.c.o:
	$(GCC) $(INCLUDES) $(CFLAGS) -c $< -o $@

$(OUT): $(OBJ)
	ar rcs $(OUT) $(OBJ)

clean:
	rm -f $(OBJ) $(OUT)
