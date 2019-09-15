.PHONY: all build doxygen

all: build doxygen
	python3 version_check.py

build:
	rm -rf build/*/.pio
	# Workaround for https://github.com/platformio/platformio-core/issues/2573
	cd build/example-DigitalIO && pio lib install uuid-common uuid-log
	platformio run -d build/example-DigitalIO

doxygen:
	wget https://raw.githubusercontent.com/nomis/mcu-uuid-doxygen/master/Doxyfile -O Doxyfile
	rm -rf html
	(cat Doxyfile; echo INPUT += ../src) | doxygen - 1>doxygen.out 2>doxygen.err
	cat doxygen.err
	cmp /dev/null doxygen.err
