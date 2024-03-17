.PHONY: all build doxygen registry
SHELL=/bin/bash

all: build doxygen
	python3 version_check.py

build:
	rm -rf build/*/.pio
	# Workaround for https://github.com/platformio/platformio-core/issues/2573
	cd build/example-DigitalIO && pio lib install --no-save nomis/uuid-common nomis/uuid-log
	platformio run -d build/example-DigitalIO

doxygen:
	wget https://raw.githubusercontent.com/nomis/mcu-uuid-doxygen/main/Doxyfile -O Doxyfile
	rm -rf html
	(cat Doxyfile; echo INPUT += ../src) | doxygen - 1>doxygen.out 2>doxygen.err
	cat doxygen.err
	cmp /dev/null doxygen.err

registry:
	diff -U0 <(git tag | sort -n) <(platformio pkg show nomis/uuid-telnet | grep -A 1000000 -E ^Version | tail -n +3 | grep -vE '^$$' | awk '{print $$1}' | sort -n)
