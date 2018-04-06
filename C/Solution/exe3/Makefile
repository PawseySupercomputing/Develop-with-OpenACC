CC=pgcc
ifeq ($(VIS),1)
	INC=-DVIS -I../../include/
endif
ACC_FLAGS=-fast -Minfo=all -acc
CFLAGS=$(ACC_FLAGS) -DROWS=2000 -DCOLS=2000 $(INC)
all: heat_eq_v2

heat_eq_v2: heat_eq.o
	$(CC) $(CFLAGS) heat_eq.o -o heat_eq_v2 

%.o: %.c
		$(CC) -c -o $@ $< $(CFLAGS)

clean:
		rm *.o heat_eq_v2
cleanall:
		rm *.o *.out *.vtk heat_eq_v2
