# K_memeset int32 and regs
K_memeset int32 and regs are components only accessibe in the c coding view and they allow for endless possibilyties.

## K_memset
K_memset is used to fill memory regions with a value

```C
k_memset((char *)0xA0000 + (Y*320+X), Color, 1);
```
the example code shown draws a pixel in the video buffer (that starts at 0xA0000) with the position X,Y. as second parameter is passed the value to set that in this case is the Color and the third value is the number of addresses to set in this case 1 because it's only one pixel

## int32
int32 is used to call interrupts

```C
int32(0x10, &regs);
```
the example code shown swiches between VGA and TUI mode, the first argument is the interrupt to call and the second one is the register instance to use (it should always be referenced with & before the variablename)

## regs
regs are a set of value used by interrupts

```C
regs16_t regs;
```
the example shown above is how you can define an instance of regs, some fuctions like `k_InitVGA` and `k_waitKey` need regs as an argument, regs should alway be passed as a reference (`&`).
regs have different values, they are di, si, bp, sp, bx, dx, cx, ax, gs, fs, es, ds and eflags. those value can be setted like this
```C
regs.ax = 0x0000;
```

and retrived like this
```C
return regs.ax; //return is not necessary
```
## Correlated:
- [C coding](https://samma2009.github.io/NovilleOSM/Ccoding)
- [Drawing functions in C]()
- [input functions in C](https://samma2009.github.io/NovilleOSM/inputC)
