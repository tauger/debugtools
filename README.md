Tool #1: gcc -finstrument-functions flag
https://balau82.wordpress.com/2010/10/06/trace-and-profile-function-calls-with-gcc/

To use it,
$ gcc -finstrument-functions -g -c -o foo.o foo.c
$ gcc -c -o trace.o trace.c
$ gcc foo.o trace.o -o foo
$ ./foo

$ ./readtracelog.sh foo trace.out

