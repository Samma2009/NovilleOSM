# input functions in C
there are a lot of input / output functions that you can use in Noville, some of those are the waitkey function or the printf function, we will se them in detial

## k_clear_screen
k_clear_screen clears the cli console

```C
k_clear_screen();
```
using k_clear_screen as shown in this example will clear the console in TUI mode.

## k_printf and k_println
k_printf and k_println are both similar functions, k_printf prints a string to the CLI and k_println prints a string to the CLI and then returns to a new line

```C
k_printf("prints ");
k_prinln("prints and returns");
```
the example code shown prints "prints prints and returns" because the first function called (`k_printf`) does not return

## k_waitKey and ReadKey
like k_printf and k_println they are similar fuctions, k_waitKey waits for a key and ReadKey waits for a key and then returns the character corrisponding the the key value. they bot need a reference of regs to work

```C
k_waitKey(&regs);
char * val = ReadKey(&regs);
```
the example code shown waits for a key and then reads another key can stores it to val

## strlen
strlen returns the lenght of a string

```C
int length = strlen("abc");
```
the example code shown gets the lenght of "abc" that will be 3 and stores it into the lenght variable

## numberToString
numberToString turns an integer to a string

```C
char * val = numberToString(5);
```
the example code shown turns the int 5 into a string, in this case "5" and then stores into val

## append
append appends two strings

```C
char * val = append("a","b");
```
the example code shown appends the strings "a" and  "b", geiving the result of "ab", it then gets stored to val

## SetCursorPos
SetCursorPos set the position of the virtual cursor in CLI mode

```C
SetCursorPos(X,Y);
```
the example code shown set the virual cursor's position to X and Y

## Correlateds
- [C coding](https://samma2009.github.io/NovilleOSM/Ccoding)
- [Drawing functions in C]()
- [k_memset int32 and regs](https://samma2009.github.io/NovilleOSM/Kadvanceds)
