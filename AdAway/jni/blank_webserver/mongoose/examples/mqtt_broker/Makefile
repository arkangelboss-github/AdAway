PROG = mqtt_broker
SOURCES = $(PROG).c ../../mongoose.c
CFLAGS = -W -Wall -I../.. -pthread -DMG_ENABLE_SSL -DMG_ENABLE_MQTT_BROKER -lssl -lcrypto $(CFLAGS_EXTRA)

all: $(PROG)

$(PROG): $(SOURCES)
	$(CC) $(SOURCES) -o $@ $(CFLAGS)

$(PROG).exe: $(SOURCES)
	cl $(SOURCES) /I../.. /DMG_ENABLE_SSL /DMG_ENABLE_MQTT_BROKER /MD /Fe$@

clean:
	rm -rf *.gc* *.dSYM *.exe *.obj *.o a.out $(PROG)
