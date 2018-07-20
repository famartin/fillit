# fillit
Fillit is a project that allows you to discover and / or familiarize yourself with a recurrent problem in programming: the search for an optimal solution among a very large number of possibilities, within a reasonable time. In the case of this project, it will be a question of arranging Tetriminos between them and to determine the smallest possible square that can accommodate them.

# General instructions
* Your project must be written in C and must respect the Norme coding standard.
* The allowed functions are : exit, open, close, write, read, malloc and free.
* Your Makefile must compile your code without relinks.
* It must contain the following rules : all, clean ,fclean et re.
* You must compile your binary with the Wall, Wextra and Werror flags. Any other
flag are forbidden , especially those for optimising purposes.
* The binary must be named fillit and located in the root directory of your repository

# Mandatory Part
Your executable must take only one parameter, a file which contains a list of Tetriminos
to assemble. This file has a very specific format : every Tetrimino must exactly fit in a
4 by 4 chars square and all Tetrimino are separated by an newline each.
If the number of parameters sent to your executable is not 1, your program must display
its usage and exit properly. If you don’t know what a usage is, execute the command
cp without arguments in your Shell. It will give you an idea. Your file should contain
between 1 and 26 Tetriminos.

The description of a Tetriminos must respect the following rules :
* Precisely 4 lines of 4 characters, each followed by a new line (well... a 4x4 square).
* A Tetrimino is a classic piece of Tetris composed of 4 blocks.
* Each character must be either a block character(’#’ ) or an empty character (’.’).
* Each block of a Tetrimino must touch at least one other block on any of his 4 sides
(up, down, left and right).

# The smallest square
The goal of this project is to arrange every Tetriminos with each others in order to make
the smallest possible square. But in some cases, this square should contains holes when
some given pieces won’t fit in perfectly with others.
Even if they are embedded in a 4x4 square, each Tetrimino is defined by its minimal
boundaries (their ’#’). The 12 remaining empty characters will be ignored for the
Tetriminos assemble process.
Tetriminos are ordered by they apparition order in the file. Among all the possible
candidates for the smallest square, we only accept the one where Tetriminos is placed on
their most upper-left position.

# Program output
Your program must display the smallest assembled square on the standard output. To
identify each Tetrimino in the square solution, you will assign a capital letter to each
Tetrimino, starting with ’A’ and increasing for each new Tetrimino.
If the file contains at least one error, your program must display error on the standard
output followed by a newline and have to exit properly.
