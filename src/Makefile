.DEFAULT_GOAL = staw
.PHONY = clean
.PHONY = install

CC = clang
CFLAGS = -O2 -Wall -Wextra -std=c11
OBJECTS = staw.o


loadingnewyear: $(OBJECTS)
	$(CC) $(LDFLAGS) -o loadingnewyear $(OBJECTS)

%.o: %.cpp
	$(CC) $(CFLAGS) -c $^ -o $@

clean:
	@rm $(OBJECTS) 2> /dev/null || exit 0

install: staw
	@sudo cp staw /usr/bin/ && \
		echo "Installed, Thank you!"
