# RACK42 - A Spreadsheet Application for the DM42
## The unique (RPN) Spreadsheet for/in your Pocket!
---
## COMING SOON!
---

```
This software is protected by the BSD 3-Clause License and
copyright (c) 2015-2021, SwissMicros. All rights reserved.

Changes and additions are protected by the BSD 3-Clause License
and made by deetee, (c) 2022. All rights reserved.

---

____________________

 PREAMBLE
____________________

The DM42 calculator is a genuine device. A brilliant LCD display, good keys, a
USB disk and a powerful processor - all low powered by a single battery cell.
On the very stable operating system (DMCP) runs Free42 - a perfect simulator of
the legendary HP42 calculator.

As the DM42 is an "open system" it is possible to run other software on top of
the operating system (DMCP). And that is, where RACK42 comes in. With RACK42
you can load and run a small, fast, simple, convenient and powerful spreadsheet
application - and probably it is the only one that uses the RPN calculation mode.
When editing a cell the formula will be evaluated and shown instantly
("Calculator Mode").


Have fun!
deetee


____________________

 SCREEN
____________________

The top line of the screen (status line) shows the selected cell address, the
value of this cell (if demanded with DISP), some indicators (shift, reference or
ascii character selection) and the battery status (0...9).
The second line (edit line) shows the content (formula or text) of the selected
cell.
The third part of the screen swows the spreadsheet (with a cell width of 9) or
(when editing a text) all available ascii characters.
At the bottom of the screen the function keys are shown.
Please note that in case of printing a chart (see chapter Graphics) thw whole
screen is used by the chart.


____________________

 SPECIFICATIONS
____________________

  6 15   Number of columns and rows
  3 5    Number of columns and rows to be printed
  26     Size of calculation stack
  50     Number of commands per cell
  9      Cell width


____________________

 NAVIGATION MODE
____________________

When starting RACK42 you are in the navigation mode. The number keys work as
cursor pad (see below). You can select and edit a specific cell, recalculate the
entire spreadsheet, save or load specific files or copy and paste a cell.
The navigation mode is also active when you refere in a formula to a specific
cell (see edit mode).

Navigation Numpad/Cursorpad:
  7 Home  8 Up     9 PgUp
  4 Left  5 Enter  6 Right
  1 End   2 Down   3 PgDn

Keys in navigation mode:
  1...9            Navigation - cursor pad
  ALPHA STO        Define and edit a new text cell
  EDIT/F1 ENTER 5  Edit selected cell
  CALC/F2 XEQ      (Re-)Calculate spreadsheet
  SAVE/F3 ^        Save recent spreadsheet to file new.s (dir RACK42 exists)
  LOAD/F4 v        Load spreadsheet from USB disk (dir RACK42 exists)
  COPY/F5          Copy selected cell to clipboard
  PASTE/F6         Paste cell from clipboard
  PRINT            Print graphic (see below)
  BACKSPACE        Delete cell content

  DISP             Show grid
  SHOW             Show cell value in status line
  SETUP            Quit to DMCP
  EXIT             On/Off (Suspend)


____________________

 EDIT MODE (FORMULA)
____________________

When in (formula) edition mode you can type a formula in RPN mode. The formula
will be evaluated instantly and the value is shown in the cell or (if with DISP
demanded) in the status line with better precision ("Calculator Mode").

Edit keys:
  ENTER/F1   Enter formula and exit edit mode (to navigation mode)
  R/S Sep/F2 Separate numbers
  REF/F3 RCL Insert reference cell (select: ENTER/F1, escape: ESC/F3)
  CLR/F4     Clear complete formula
  <-/F5      Edit cursor left
  ->/F6      Edit cursor right
  BSPC       Delete command

  1...9.     Insert number
  + - * /    Basic operation
  X<>Y       Swap stack register
  +/-        Negate TOS (NEG)
  E          Push 10^TOS to the stack
  Rv         Rotate
  MATH       1/X SQRT LOG LN POW SQR 10^X e^X
  TRIG       SIN COS TAN ASIN ACOS ATAN
  SUM+       Sum of range
  SUM-       Count of range


____________________

 EDIT MODE (TEXT)
____________________

When defining (ALPHA or STO) or editing (EDIT, ENTER/F1) a text cell all
possible characters will be shown an can be selected using the navigtion pad.

  ENTER/F1 STO Enter text and exit text mode (to navigation mode)
  INS/F2 5     Insert selected character to text
  CLR/F4       Clear complete text
  <-/F5        Edit cursor left
  ->/F6        Edit cursor right
  BSPC         Delete character
  NAVIGATE     Use navigation pad to select character


____________________

 GRAPHICS
____________________

RACK42 can display a simple bar graphic. Enter the desired text (optional) and
the  related data in two colums. Define in another cell the range of the data
column (references to first and last data cell). Navigate to this "reference
cell" and press PRINT to view a simple bar chart. As the bars are scaled the
maximum value will be printed in the first line. Please note that bars with
negative values are not printed.


____________________

 ASCII TABLE
____________________

  DEC     |  0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5
      HEX |  0 1 2 3 4 5 6 7 8 9 a b c d e f
  ------------------------------------------
  032 20  |    ! " # $ % & ' ( ) * + , - . /
  048 30  |  0 1 2 3 4 5 6 7 8 9 : ; < = > ?
  064 40  |  @ A B C D E F G H I J K L M N O
  080 50  |  P Q R S T U V W X Y Z [ \ ] ^ _
  096 60  |  ` a b c d e f g h i j k l m n o
  112 70  |  p q r s t u v w x y z { | } ~
  128 80  |  D M S I G S T P Q L L G N E D R
          |  I U Q N R I A I M E F E E N O I
          |  V L R T E G B             T W G
          |    T T   Y M               E N H
          |          1 A               R   T
  144 90  |  L M P G A N A A E A 3 E O U G S
          |  E U O R O T U N   E D S U U R Q
          |  F   U A   I M G     O C M M E A
          |  T   N D   L L L     T   L L Y R
          |      D     D   E     S       2 E
  160 A0  |  T T
          |  R R
          |  I I
          |  D U




```
