all:
	g++ -c *.cpp
	g++ *.o -o a.out

run: all
	./a.out

clean:
	rm -f *.o
	rm -f *.out
	rm -f valgrind-log.txt

gdb:
	g++ *.cpp -g
	gdb ./a.out

valgrind:
	g++ *.cpp -g
	valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes --verbose --log-file=valgrind-out.txt ./a.out > valgrind-log.txt
	nano valgrind-out.txt
