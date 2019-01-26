# The basics of BASIC
Introduction to CBM BASIC


by Daniele Olmisani
and the contributions of @JaganGanesh

Please, see [LICENSE](LICENSE) file.

## Hello World!
```bas
PRINT "HELLOWORLD!"
```

## Simple Arithmetic

```bas
PRINT 3+3, 3-3, 3*3, 3/3, 3^3
```

Operator are evaluated left-to-right with this predence order: ^, */, +-.

```bas
PRINT 9*8+7+6^5/4-3-2+1
```

## Built-in Functions

Square function and natural logarithm with the basis E

```bas
PRINT SQR(4), 4*4
```

```bas
PRINT LOG(1), LOG(100)/LOG(10)
```

## Build-in Constants

Pi value

```bas
PRINT {PI}
```

## Logic operations

Equality operators =, <>, >, >.

```bas
PRINT 1=1, 1=0, 1<>1, 1<>0
```

```bas
PRINT 1>0, 1<0
```

True and False values are represented by numeric values -1 and 0.

Built-in operators AND, OR and NOT.

```bas
PRINT 0 AND 0, -1 AND 0, 0 AND -1=1, -1 AND -1
```

```bas
PRINT 0 OR 0, -1 OR 0, 0 OR -1=1, -1 OR -1
```

```bas
PRINT NOT 0, NOT -1
```

XOR operator is not included but it shall be derived using formula (p|q) & ~(p&q).

```bas
10 PRINT "P", "Q", "P XOR Q"
20 FOR P=0 TO 1
30 FOR Q=0 TO 1
40 : PRINT P, Q, (P OR Q) AND NOT(P AND Q)
50 NEXT Q
60 NEXT P
```

## FOR-NEXT Loop
```bas
10 FOR I = 1 TO 4
20 PRINT "HELLOWORLD!"
30 NEXT I
```

## INPUT Variables
```bas
10 DIM A$(1)
20 PRINT "PRESS RETURN TO CONTINUE"
30 INPUT A$
```

```bas
10 DIM N$(40)
20 PRINT "WHAT IS YOUR NAME: ";
30 INPUT N$
40 PRINT "HELLO, "; N$
```

## IF Condition
```bas
10 DIM A$(4)
20 PRINT "DO YOU LIKE C64: ";
30 INPUT A$
40 IF A$ = "YES" THEN 60
50 END
60 PRINT "GREAT!"
70 GOTO 50
```

## Random Numbers
```bas
10 PRINT RND(1)
```

```bas
10 PRINT INT(10*RND(1) + 1)
```

## GOSUB
```bas
10  PRINT "HELLO"
20  GOSUB 100
30  END
100 PRINT "WORLD"
110 RETURN
```
