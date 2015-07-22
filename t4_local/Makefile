
prefix ?= /tmp/t3/usr

# all: build install
all: build

build:
	mkdir -p build
	cd build; cmake -DCMAKE_INSTALL_PREFIX=${prefix} ..
	cd build; make

# Install library, header
install:
	make -C build install

clean:
	rm -rf build
