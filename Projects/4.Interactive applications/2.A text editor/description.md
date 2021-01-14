# Projecto 2. Simple text editor

You are going to build an interactive program that allows writing up to 10 lines of text, with a maximum of 15 characters per line.
In order to do that, we will use the following representation:

 * The current position of the head will represent the place where the cursos is located, that is, where the next character will be written.
 * The letters are represented as in the activity _“Representing characters”_: with black stones, 1 for ‘A’, 2 for ‘B’, etc.
 * The space character is represented as an empty cell (that is, 0 black stones…).
 
Every time a letter between ‘A’ and ‘Z’ is pressed, that letter must be written in the board (without forgetting to erase the previous 
content, if there is any), and then to advance the cursor to the right. When it is not possible to advance the cursor to the right, it
must continue at the beginning of the next line.
The space bar inserts a space, and the enter key automatically goes to the beginning of the next line.
It is also desirable that the cursor can be moved using the arrows, without altering the text. 
The program must NOT fail (make BOOM) in any situation: if some operation associated with a key cannot be done for any reason, the program
must ignore it, and do nothing.

In this editor, when a character is written, the previous content of the cell is overwritten -- it is not needed to move the text when 
adding or removing characters, because that requires a more complex work.

Rembember to always divide into subtasks, and to use parameteres when needed. 
¿How about the idea of making procedures called `DrawCharacter`, `AdvanceCursor`, `GoToANewLine` y `ClearCell` 
and functions `codeOfLetterA`, …, `codeOfLetterZ` y `codeOfSpace` to be used as arguments of `DrawCharacter`? 
Remember that before drawing a character, the cell must be clears, and that after drawing it, the cursor must be advanced 
-- without forgetting that `AdvanceCursor`, if there is no more room in the line, must go to a new line.

> **Hint**
>
> Several of the procedures that you will need were already built in previous activities -- for example, those of clearing the cell, advancing
> the cursor, and drawing characters are similar to those of _“Representing characters”_, (¡but now some of them with parameters!). 
> It may be useful to look for them, and use them as models, so you do not have to think them all over!
