CXX=clang++-3.5
CXXFLAGS=-g -std=c++11 -Wall -pedantic \
-I/home/roman/Documents/DP/caffe/distribute \
-I/home/roman/Documents/DP/caffe/include/ \
-DCPU_ONLY
LIBS=-L/home/roman/Documents/DP/caffe/build/lib -Wl,-R/home/roman/Documents/DP/caffe/build/lib \
-lcaffe -lboost_system \
-lglog \
`pkg-config opencv --cflags --libs`


all: disparity_map_estimation
	
disparity_map_estimation.o: disparity_map_estimation.cpp
	$(CXX) -c $(CXXFLAGS) disparity_map_estimation.cpp

disparity_map_estimation: disparity_map_estimation.o
	$(CXX) -o disparity_map_estimation disparity_map_estimation.o $(CXXFLAGS) $(LIBS)

clean:
	rm *.o
