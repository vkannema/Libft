# Libft - @42Born2Code
My implementation of some of the Standard C Library functions including some additional ones.

### TOC
* [What is libft?](#what-is-libft)
* [What's in it?](#whats-in-it)
* [How does it work?](#how-does-it-work)
* [How do I use the library?](#how-do-i-use-the-library)
* [How do I test it? How do I test my own implementations?](#how-do-i-test-it-how-do-i-test-my-own-implementations)
	1. [To test the code in this repo](#1-to-test-the-code-in-this-repo)
* [Example usage](#example-usage)

### What is libft?
Libft is an individual project at 42 that requires us to re-create some standard C library functions including some additional ones that can be used later to build a library of useful functions for the rest of the program.

Disclaimer: *Reinventing the wheel is bad, 42 makes us do this just so we can have a deeper understanding of data structures and basic algorithms. At 42 we're not allowed to use some standard libraries on our projects, so we have to keep growing this library with our own functions as we go farther in the program.*

### What's in it?

As you can see from the [Project instructions][1], there are 4 sections:

1.  **Libc Functions:** Some of the standard C functions
2.  **Additional functions:** Functions 42 deems will be useful for later projects
3.  **Bonus Functions:** Functions 42 deems will be useful for linked list manipulation
4.  **Personal Functions:** Functions I believe will be useful later.

Libc functions | Additional functions | Bonus Functions | Personal Functions
:----------- | :-----------: | :-----------: | -----------:
memset		| ft_memalloc	| ft_lstnew		| ft_capitalize
bzero		| ft_memdel		| ft_lstdelone	| ft_countwords
memcpy		| ft_strnew		| ft_lstdel		| ft_islower
memccpy		| ft_strdel		| ft_lstadd		| ft_isupper
memmove		| ft_strclr		| ft_lstiter	| ft_strndup
memchr		| ft_striter	| ft_lstmap		| ft_lst_reverse
memcmp		| ft_striteri	|				| ft_realloc
strlen		| ft_strmap		|				| ft_strjoinch
strdup		| ft_strmapi	|				| ft_strnchr
strcpy		| ft_strequ		|				| ft_copyuntil
strncpy		| ft_strnequ	|			| [ft_printf functions][4]
strcat		| ft_strsub		| | ft_intlen
strlcat		| ft_strjoin	| | ft_strendswith
strchr		| ft_strtrim	| | ft_pathjoin
strrchr		| ft_strsplit	| | ft_lstaddback
strstr		| ft_itoa		|
strnstr		| ft_putchar	|
strcmp		| ft_putstr		|
strncmp		| ft_putendl	|
atoi		| ft_putnbr		|
isalpha		| ft_putchar_fd	|
isdigit		| ft_putstr_fd	|
isalnum		| ft_putendl_fd	|
isascii		| ft_putnbr_fd	|
isprint		|
toupper		|
tolower		|


Notes:

- All the files and functions are namespaced with an **ft** in front. It stands for Fourty Two

My code is not the best, but it passed all the 42 tests successfully.

### How does it work?

The goal is to create a library called libft.a from the source files so I can later use that library from other projects at 42.

To create that library, after downloading/cloning this project, **cd** into the project, copy all the files from the sub folders to the root directory and finally, call make:

	git clone https://github.com/vkannema/Libft/
	cd Libft
	make

You should see a *libft.a* file and some object files (.o).


Now to clean up (removing the .o files and the .c files from the root), call `make clean`

### How do I use the library?

You have to tell the file where your library resides and which library it is using:

`gcc -L. -lft example.c`

-L takes the path to your library. `.` in this case<br>
-l takes the name of your library. This is the set of characters that come after `lib` in your library name.

That's it. Now run it using `./a.out`

### How do I test it? How do I test my own implementations?

To test the code we're going to be using @alelievr's [Libft Unit Test][1].

#### 1. To test the code in this repo

1. Clone this repo and cd into it, make sure it's called `libft`:

		git clone https://github.com/vkannema/Libft/
		cd Libft/
    
2. Run Make so you can build the library:

		make
3. Go back to the root directory and download @alelievr's Libft Unit Test:

		cd ..
		git clone https://github.com/alelievr/libft-unit-test
4. Go into the test folder and run the test:

		cd libft-unit-test/
		make f

If you did everything correctly you should get a cool list of tests showing you the function names and if they passed or not.

That's it! If you're having some problems, just [send me a tweet][2]. If you think your problem is due to my code or this README, [create a new issue][3]. I'll definitely check it out.

[1]: https://github.com/alelievr/libft-unit-test
[2]: https://twitter.com/kannemacher
[3]: https://github.com/vkannema/libft/issues
[4]: https://github.com/vkannema/ft_printf
