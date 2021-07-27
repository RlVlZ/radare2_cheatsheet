# Debug mode

### # Launch radare2 in debugging mode :
```
r2 -d mybinary
```
If mybinary expect some arguments :
```
r2 -d mybinary arg1 arg2 ...
```

### # Start analysing the binary :
```
aaa
```
Note that according to **pancake** there are better ways to get started (see [here](https://www.youtube.com/watch?v=tE5AKOQgIe4))

### # Set breakpoints :
```
db my_function
```
also works with raw adresses.

### # Get the program running :
step by step : 
```
s
```
step over :
```
S
```
continue (untill breakpoint or end of process) :
```
dc
```

### # Restart the process :
```
doo
```
if the binary expects arguments :
```
doo arg1 arg2
```

### # Visual mode :
```V``` will bring you to Visual mode. You first have some hexDump of the binary, which is not that usefull. You can navigate through different view using ```p```.
The third view is probably the best as it shows dissassembly, registers and the stack.
However I prefer VISUAL PANEL mode.

### # Visual Panel Mode :

```V!``` will bring you to the VisualPanelMode ! There you need a few commands to get comfortable :
  - Navigate the != splits with \<TAB\>
  - Close a pannel with ```X```
  - Change the content of a pannel with ```"``` and navigate the choices with hjkl
  - Create a vertical split with ```|```
  - Create an horizontal split with ```-```
  - Resize splits by entering window mode : ```w``` and then unsing HJKL (quit window mode with q)
  - Save you new Layout by entering the menu bar (on top) : ```m```, then enter the "File" submenu with \<ENTER\> and go to save Layout

### # Memory modification :
You can write into registers using the following :
```
wr rip 0x01
```
