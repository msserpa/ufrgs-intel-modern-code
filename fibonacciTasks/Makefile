COMPILER = icc
FLAGS = -lm -no-vec -qopenmp -xHost -Wall -Wextra

all: fibonacciTask.exec fibonacciTaskPar.exec
	@echo "Compiled!"

%.exec: %.o
	$(COMPILER) -o $@ $+ $(FLAGS)

%.o: %.c
	$(COMPILER) -o $@ -c $< $(FLAGS)

clean:
	rm -f *.o *.exec *.optrpt
