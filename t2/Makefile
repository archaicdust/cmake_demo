# out-of-source build

prefix ?= /tmp/t2/usr

all: build install


build:
	mkdir build
	cd build; cmake -DCMAKE_INSTALL_PREFIX=${prefix} ..
	make -C build

install:
	make -C build install

clean:
	rm -rf build
	#rm -rf /tmp/t2/usr
