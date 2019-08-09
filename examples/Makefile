all: demo

CUPTI_PATH=/usr/local/cuda/extras/CUPTI
INCLUDES = -I ../include -I /usr/local/cuda/extras/CUPTI/include
CXXARGS = -std=c++11 -g
CXXARGS += -Xcompiler -DNDEBUG
LIBS = -lcuda -L$(CUPTI_PATH)/lib64 -lcupti

demo: CUPTI_Conv.cu
	#nvcc $(CXXARGS) $(INCLUDES) $(LIBS) CUPTI_Conv.cu -o demo
	nvcc $(CXXARGS) $(INCLUDES) $(LIBS) CUPTI_Conv100.cu -o demo
	#nvcc $(CXXARGS) $(INCLUDES) $(LIBS) CUPTI_vector_multiply.cu -o demo
	# nvcc $(CXXARGS) $(INCLUDES) $(LIBS) CUPTI_matrix_multiply.cu -o demo
	#  nvcc $(CXXARGS) $(INCLUDES) $(LIBS) CUPTI_vector_add.cu -o demo

clean:
	rm -f *.o demo
