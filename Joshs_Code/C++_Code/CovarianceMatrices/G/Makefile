LD=g++
LDFLAGS=-L/usr/lib64 -lfftw3 -g -L/usr/lib64 -lgsl -lgslcblas -L/home/jsdillon/Libraries/FFTW/lib -L/home/jsdillon/Libraries/GSL/lib 
CXXFLAGS= -g
IFLAGS = -I/home/jsdillon/Libraries/GSL/include/ -I/home/jsdillon/Libraries/FFTW/include/

G : G.o ../../CommonClasses/Specs.o ../../CommonClasses/CVector.o 
	$(LD) -o $@ $^ $(LDFLAGS)

G.o : G.cpp  ../../CommonClasses/Specs.h ../../CommonClasses/CVector.h
	$(LD) $(IFLAGS) -c $^ $(LDFLAGS)

../../CommonClasses/CVector.o : ../../CommonClasses/CVector.cpp ../../CommonClasses/CVector.h ../../CommonClasses/Specs.h
	$(LD) $(IFLAGS) -c $^ $(LDFLAGS)

../../CommonClasses/Specs.o: ../../CommonClasses/Specs.cpp ../../CommonClasses/Specs.h

.dummy clean :
	rm -f G *.o