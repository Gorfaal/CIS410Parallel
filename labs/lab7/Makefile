default: matmul_serial matmul_improved matmul_cilk

all: matmul_serial matmul_mp matmul_cilk matmul_tbb

matmul_serial: matmul.c
	icc -o matmul_serial matmul.c -fopenmp

matmul_improved: matmul_improved.c
	icc -o matmul_improved matmul_improved.c -fopenmp

matmul_mp:

matmul_cilk: matmul_cilk.c 
	icc -std=c99 -o matmul_cilk matmul_cilk.c -lcilkrts -fopenmp

matmul_tbb:

clean:
	rm matmul_serial matmul_mp matmul_cilk matmul_tbb 2>/dev/null
