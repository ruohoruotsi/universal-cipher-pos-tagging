# 1.2: need to make sure opt.o goes in the right order to get the right scope on the command-line arguments
# Use this for Linux
files=$(subst .cc,.o,$(shell /bin/ls basic/*.cc))

all: marlin_cluster

marlin_cluster: marlin_cluster.o $(files)
	g++ -std=c++11 -Wall -g -O3 -o marlin_cluster marlin_cluster.o $(files)

%.o: %.cc
	g++ -Wunused -std=c++11 -Wall -g -O3 -o $@ -c $<

clean:
	rm -rf marlin_cluster basic/*.o *.o
