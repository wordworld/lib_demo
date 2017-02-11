CXXTEST = $(HOME)/git/cxxtest

TESTS = MyTestSuite1.h MyTestSuite2.h
GEN_FILE = $(TESTS:.h=.cpp)
BIN = $(TESTS:.h=.exe)

all:$(BIN)

$(BIN):$(GEN_FILE)
	g++ -I$(CXXTEST) $< -o $@

.h.cpp:
	cxxtestgen --error-printer $< -o $@

clean:
	rm -f $(GEN_FILE) $(BIN)
