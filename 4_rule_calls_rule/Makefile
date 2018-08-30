DEST1 = file1.out
DEST2 = file2.out
DEST = $(DEST1) $(DEST2)

all: $(DEST)

$(DEST):
	$(MAKE) write1
	$(MAKE) write2

write1:
	echo 'some text 1' > $(DEST1)

write2:
	echo 'some text 2' > $(DEST2)
