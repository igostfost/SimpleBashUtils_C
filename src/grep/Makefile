CC=gcc
CFLAGS=-Wall -Werror -Wextra
CLANGC=clang-format -i *.c
CLANGH=clang-format -i *.h

all: s21_grep

rebuild: clean all

s21_grep: s21_grep.c
	$(CLANGC)
	$(CLANGH) 
	$(CC) $(CFLAGS) s21_grep.c -o s21_grep

fsanitize: 
	$(CC) $(CFLAGS) s21_grep.c -o s21_grep -fsanitize=address

valgrind: test
	valgrind --track-origins=yes --leak-check=full --show-leak-kinds=all ./s21_grep


clean:
	rm -f s21_grep