CC=gcc
CFLAGS=-Wall -Werror -Wextra
CLANGC=clang-format -i *.c
CLANGH=clang-format -i *.h

all: s21_cat

rebuild: clean all

s21_cat: s21_cat.h s21_cat.c
	@$(CLANGC)
	@$(CLANGH) 
	@$(CC) $(CFLAGS) s21_cat.c -o s21_cat

test: clean s21_cat
	bash TEST_CAT_mac.sh

clean:
	@rm -f s21_cat
