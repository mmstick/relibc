BINS=\
	args \
	create \
	write

all: $(BINS)

clean:
	rm -f $(BINS) *.out

run: $(BINS)
	for bin in $(BINS); do echo "\\033[1m$${bin}\\033[0m"; ./$${bin} test args; done

%: %.c
	gcc -nostdinc -nostdlib -I ../include -I ../target/include ../target/debug/libcrt0.a $< ../target/debug/libc.a -o $@