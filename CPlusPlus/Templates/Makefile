CXX = g++
CXXFLAGS = -O2 -g -Wall -Wextra -std=c++14
LDLIBS = -lm

.PRECIOUS: %.o

APPL = swap.exe sum.exe points.exe pendulum_func_obj.exe pendulum_bind.exe \
       pendulum_lambda.exe print_container.exe \
       print_container_no_range_for.exe fac.exe

all: $(APPL)

pendulum_func_obj.exe: pendulum_func_obj.o pendulum_utils.o
	$(CXX) $(CXXFLAGS) -o $@ $^ $(LDLIBS)

pendulum_bind.exe: pendulum_bind.o pendulum_utils.o
	$(CXX) $(CXXFLAGS) -o $@ $^ $(LDLIBS)

pendulum_lambda.exe: pendulum_lambda.o pendulum_utils.o
	$(CXX) $(CXXFLAGS) -o $@ $^ $(LDLIBS)

%.exe: %.o
	$(CXX) $(CXXFLAGS) -o $@ $^ $(LDLIBS)

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c -o $@ $<

clean:
	rm -f *.o $(APPL)
