CXX=clang++-3.5
CXXFLAGS=-g -std=c++11 -Wall -pedantic \
-I/home/roman/Documents/DP/caffe/distribute \
-I/home/roman/Documents/DP/caffe/include/ \
-DCPU_ONLY
LIBS=-L/home/roman/Documents/DP/caffe/build/lib -Wl,-R/home/roman/Documents/DP/caffe/build/lib \
/home/roman/Documents/DP/caffe/build/lib/libcaffe.so \
-lcaffe -lboost_system

all: disparity_map_estimation
	
disparity_map_estimation.o: disparity_map_estimation.cpp
	$(CXX) -c $(CXXFLAGS) disparity_map_estimation.cpp

disparity_map_estimation: disparity_map_estimation.o
	$(CXX) $(CXXFLAGS) -o disparity_map_estimation disparity_map_estimation.o $(LIBS)

clean:
	rm *.o
