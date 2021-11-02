# GDBPythonLearn

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




#assembly
-setb: set if below, use after cmp
