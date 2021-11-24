# GDBPythonLearn

set output-radix 16 (and set output-radix 10 to switch it back)

## Basic GDB commands:
-Get a core file: (gdb) gcore

-Backtrace:
  +(gdb) py-bt
  +(gdb) py-bt-full
  +(gdb) bt
  
-Move up and down the call stack:
  *(gdb) up
  *(gdb) down
  
-Show local variables in the stack frame:
  +(gdb) info locals
  +(gdb) info args
 
-Show surrounding python source:
 +(gdb) py-list
 +(gdb) list
  
-show all threads:
 +(gdb) info threads




# assembly </br>
-setb: set if below, use after cmp
Ex: setb al
set al to 1


# breakpoint in GDB

## see register value:
```
(gdb) p $rbx
$23 = 140737488348072
(gdb) python print type(gdb.parse_and_eval("$rbx")), gdb.parse_and_eval("$rbx")
<type 'gdb.Value'> 140737488348072
```

</br>

```
(gdb) info register rip
rip            0x7f68656c142d       0x7f68656c142d <__lll_lock_wait+29>
(gdb) python print(gdb.selected_frame().read_register('rip'))
0x7f68656c142d <__lll_lock_wait+29>
(gdb) 
```
