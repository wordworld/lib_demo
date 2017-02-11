CXXTEST = $(HOME)/git/cxxtest

HEADER= MyTestSuite1.h MyTestSuite2.h
SOURCE= $(HEADER:.h=.cpp)
OBJ = $(HEADER:.h=.o)

all:$(OBJ)


.cpp.o:
	g++ -I$(CXXTEST) $< -o $@

.h.cpp:
	cxxtestgen --error-printer $< -o $@

clean:
	rm -f $(SOURCE) $(OBJ)
