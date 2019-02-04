module=sparseoperations

all: ${module}.so

${module}.so: ${module}.c
	gcc -shared -pthread -fPIC -fwrapv -O2 -Wall -fno-strict-aliasing -I/usr/include/python3.6 -I/usr/local/lib/python3.6/dist-packages/numpy/core/include -o $@ $<

${module}.c: ${module}.pyx
	cythonize -a $<

.PHONY:
clean:
	rm ${module}.c ${module}.so
