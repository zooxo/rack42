# RACK42 - A Spreadsheet Application for the DM42
## "The unique (RPN) Spreadsheet (and more) for/in your Pocket!"

---

See a short video of RACK42 at: https://youtu.be/

See a short video of version 1 of RACK42 at: https://youtu.be/_lt0Zoqh0og

---
![ss0](https://user-images.githubusercontent.com/16148023/205289206-24746b7f-fe7a-42c6-8655-905f69a798ec.png)
![ss1](https://user-images.githubusercontent.com/16148023/205289208-8f8e965a-9877-480c-b9cd-e64c71259ea9.png)
![ss2](https://user-images.githubusercontent.com/16148023/205289211-d1adec6b-a240-4fdd-851a-af32182c37d2.png)
![ss3](https://user-images.githubusercontent.com/16148023/205289213-161b4a33-5394-463b-a10a-46e9b27f7ab2.png)
![ss4](https://user-images.githubusercontent.com/16148023/205289214-d6a82795-dc8f-4c48-a298-fe17334a02ff.png)
![sshex](https://user-images.githubusercontent.com/16148023/205289218-783b67e6-2fb9-47b9-8d03-3a6bffa65cfa.png)
![bar](https://user-images.githubusercontent.com/16148023/205289195-2096b464-ec0e-45da-ab49-7563f32cb34f.png)
![fnplot](https://user-images.githubusercontent.com/16148023/205289198-8ad1610a-3f67-4cea-b390-9fd1bfc74606.png)
![ted](https://user-images.githubusercontent.com/16148023/205289220-097c3e33-d7bf-41d2-af7c-099853a2e3b5.png)
![draw](https://user-images.githubusercontent.com/16148023/205289197-7fec0331-7a62-4a8f-9efa-f3d2615b84ac.png)
![hp1](https://user-images.githubusercontent.com/16148023/205289203-2935f120-bf67-4619-b24d-d038d829b11b.png)
![hp2](https://user-images.githubusercontent.com/16148023/205289204-6450635e-6875-4579-b646-afb419dafe18.png)
![game1](https://user-images.githubusercontent.com/16148023/205289199-7326f89f-af08-4b47-a844-4e4abe78ea63.png)
![game2](https://user-images.githubusercontent.com/16148023/205289201-43c426c7-11de-4aa3-a310-96cf0ef4bbfc.png)


```


____________________

 PREAMBLE
____________________

The DM42 calculator is a genuine device. A brilliant LCD display, good keys, a
USB disk and a powerful processor - all low powered by a single battery cell.
On the very stable operating system (DMCP) runs Free42 - a perfect simulator of
the legendary HP42 calculator.

As the DM42 is an "open system" it is possible to run other software on top of
the operating system (DMCP). And that is, where RACK42 comes in.

RACK42 is primarily a mobile, small, fast, simple, convenient and powerful
spreadsheet application using RPN as mathematical notation. But RACK42 evolved
to a multifunctional productive system because of useful add on applications
like a convenient calculator mode, a text file editor, an object oriented ASCII
drawing program, an emulator of the legendary HP-35 calculator and finally the
first game (?) on the DM42 (2048 like).

Have fun!
deetee


____________________

 MODES
____________________

With MODES (SHIFT+CHS) you can almost any time select one of the following
modes/applictions:
 F1 SHEET Standard spreadsheet calculation
 F2 CAL   Calculator mode (fades out the spreadsheet)
 F3 TED   Text file editor
 F4 DRAW  Simple ASCII drawing
 F5 HP35  Emulates the legendary HP35 calculator
 F6 GAME  2048-like game

Please note that you can also select a mode with XEQ, when you are in the
 spreadsheet navigation mode.

The following subchapters explain all different modes, while all other
chapters refer to the standard spreadsheet application:

____________________
_CALCULATOR_________

With MODES and CAL you can enter (or leave) a simple calculator mode
(indicated with a 'CAL' in the status line) that 'fades out' the presentation
of the spreadsheet.

When pressing STO the current value on the stack will be stored an can be
recalled anytime with RCL.

Please note that some functions or features (ie those regarding references)
are disabled.

____________________
_TED________________

With TED you can create or edit text files. The top 4 rows of the keys are used
to simulate a standard keyboard. The keyboard layout can be assigned by the user
by editing the file "/RACK42/kbd.txt".
To change for instance the default keyboard (QWERTY) to a german keyboard
(QWERTZ) you can (after saving the default keyboard with SHIFT+F6 to the USB
disk) edit /RACK/kbd.txt with your PC text file editor and change y and z (and
of course Y and Z).

TED keys:
  SHIFT F1  QUIT TED without saving
  SHIFT F2  NEW file
  SHIFT F5  HTML view of (markdown) text
  SHIFT F6  KBD^ save current keyboard to file /RACK/kbd.txt
  / * - +   Text buffer (mark1, mark2, delete, paste)
  UP        Save text to "/RACK42/tmp.txt"
  DOWN      Load text file from USB disk

Please note that when you are leaving TED (with MODES) the current text will be
saved to "/RACK42/tmp.txt".

Please note that TED uses the same procedure as the spreadsheet application to
save a textfile with a specific file name - "SAVE AS" (enter the file name in
a selected cell of the spreadsheet application and press UP after returning to
TED). Files opened (loaded) with a specific file name are still saved under
this name (when pressing UP or automatically when leaving TED).

Keyboard (top 4 rows of keys):
  FLIP   q  w  e  r  t
  ALT    a  s  d  f  g
  SHIFT  z  x  c  v  b
  ENTER SPC SPC SPC BSP

Default keyboard:
                               ___________ALT___________
                ___SHIFT___                  ___SHIFT___
        FLIP          FLIP           FLIP          FLIP
  qwert yuiop   QWERT YUIOP    12345 67890   !@#$% ^&*()
  asdfg hjkl-   ASDFG HJKL-    *+-/= ,456.   '"`/\ <=>[]
  zxcvb nm,./   ZXCVB NM,./    \$%() -123+   .,:;~ ?|_{}

HTML view:
With SHIFT F5 TED offers a html view of the edited file using the internal
web browser of the DM42 (help file viewer). TED uses some markdown signs to
produce a html file and saves it to RACK42/ted.htm.
Please note that so far TED supports 3 headers (lines starting with #, ##
and ###) and simple not nested unordered lists (lines starting with * or -).

____________________
_DRAW_______________

With DRAW you can draw simple ASCII objects (line, rectangle, horizontal and
vertical text as well as a function plot from the spreadsheet application)
on a sheet with 7x28 characters. The objects can be treated with
cut/copy/paste later on. The final picture can be saved (PRINT) to a simple
text file (print.txt) for later use (ie with a text editor like TED).

Possible keys are:
  1~9  Cursorpad (see below, 5 centers cursor)
  F1   Draw line object
  F2   Draw rectangle object
  F3   Draw horizontal text object
  F4   Draw vertical text object
  F5   Draw last function plot from spreadsheet
  F6   Save picture to a file (print.txt)
  UP   Save DRAW file (new.d) to USB disk (see SAVE AS option below)
  DOWN Load DRAW file (*.d) from USB disk
  BSP  Delete (at "hot spot") marked object
  / *  Copy draw object to clipboard (grab "hot spot" of object)
  -    Delete clipboard
  +    Paste clipboard to current cursor position

____________________
_HP-35______________

In the HP35 mode you can use an emulation of the legendary HP35 calculator.

Please note that HP35 doesn't use shifted keys. To EXIT HP35 (and return to
the standard spreadsheet calculation) simply press F1 (QUIT).


Original HP35 display and keyboard layout:
     _________________________
    |                         |
    |     -1.234567890-12     |
    |_________________________|
    |                         |
    | X^Y  log  ln   e^X  CLR |
    | SQRT arc  sin  cos  tan |
    | 1/X  X><Y ROT  STO  RCL |
    | E-N-T-E-R CHS  EEX  CLX |
    |   -     7     8     9   |
    |   +     4     5     6   |
    |   *     1     2     3   |
    |   /     0     .     PI  |
    |_________________________|

____________________
_GAME_______________

In this 2048-like game you have to shift and merge equal numbers in a 4x4 grid.

Possible keys are:
  F1      Quit
  F2      New game
  F3 4 1  Collapse left
  F4 2    Collapse down
  F5 8 5  Collapse up
  F6 6 3  Collapse right


____________________

 SCREEN
____________________

The top line of the screen (status line) shows the selected cell address, the
value of this cell (if demanded with SHOW) or the date, some indicators (ie
shift) and the battery status (0...9).
The second line (edit line) shows the content (formula or text) of the selected
cell.
The third part of the screen swows the spreadsheet (with a cell width of 9), or
two top registers of the stack or (when editing a text) all available ascii
characters.
At the bottom of the screen the function keys are shown.
Please note that in case of printing a chart (see chapter Graphics) the whole
screen is used by the chart.

Indicators:
  9                  Battery status (0~9)
  ^ (arrow up)       Shift
  -> (cursor right)  CursorPad is active
  1                  (Formula) Edit mode - NumPad is active
  SQRT               (Formula) Edit mode - Extra math menu is active
  @                  (Formula) Edit mode - Reference selection
  "                  (Text) Edit mode
  x                  HEXmode1 (status line shows cell value in hex format)
  X                  HEXmode2 (only status line shows cell value decimal)


____________________

 PRIOR KEYS
___________________

 SETUP   Quit RACK42 to operating system (DMCP)
 EXIT    On/Off (Suspend)
 SHIFT   Toggle shift key
 MODES   Modes menu (Spreadsheet, Calculator, Ted, Draw, HP-35)
 ASSIGN  Screenshot
 SHOW    Shows date/time or specific information in the status line
 DISP    Toggle grid display
 BASE    HEX mode (no HEXmode, HEXmode1 or HEXmode2)
 SST     View help image (/RACK42/RACK42help.bmp)
 BST     View html help file (/RACK42/RACK42help.htm)

____________________

 NAVIGATION MODE
____________________

When starting RACK42 you are in the navigation mode. The number keys work as
cursor pad (see below). You can select and edit a specific cell, recalculate the
entire spreadsheet, save or load specific files or copy and paste a cell.
The navigation mode is also active when you refer in a formula to a specific
cell (see edit mode).

Navigation Numpad/Cursorpad:
  7 Home  8 Up     9 PgUp
  4 Left  5 Enter  6 Right
  1 End   2 Down   3 PgDn

Keys in navigation mode:
  1~9              Navigation - cursor pad
  ALPHA STO        Define and edit a new text cell
  EDIT/F1 ENTER 5  Edit selected cell
  CALC/F2 XEQ      (Re-)Calculate spreadsheet
  SAVE/F3 ^        Save recent spreadsheet to file new.s (dir RACK42 exists) *)
  LOAD/F4 v        Load spreadsheet from USB disk (dir RACK42 exists)
  COPY/F5          Copy selected cell to clipboard
  PASTE/F6         Paste cell from clipboard
  BACKSPACE        Delete cell content
  CLEAR            Clears complete sheet
  DISP             Show grid
  XEQ              Enter mode menu
  PRINT            Print graphic (see chapter GRAPHICS)
  PGM.FCN          Function plot (see chapter CALCULUS)
  ASSIGN           Make a screenshot

  *) Please note that if the selected cell is a text cell, RACK42 saves the file
     under the filemname of this cell's text ("SAVE AS").

  **) BASE/HEXmode:
                       noHEXmode HEXmode1 HEXmode2
      Indicator        none      x        X
      Input/CellValue  decimal   decimal  hex
      Status value     decimal   hex      decimal


____________________

 EDIT MODE (FORMULA)
____________________

When in (formula) edition mode you can type a formula in RPN mode. The formula
will be evaluated instantly and the value is shown in the cell (or with big
letters as stack if with CUSTOM demanded) or (if with DISP
demanded) in the status line with better precision ("Calculator Mode").

Edit keys:
  ENTER/F1 5   Enter formula and exit edit mode (to navigation mode)
  Sep/F2 R/S   Separate numbers
  REF/F3 RCL   Insert reference cell (select: ENTER/F1, escape: ESC/F3)
  CLR/F4       Clear complete formula
  <-/F5        Edit cursor left
  ->/F6        Edit cursor right

  1...9.       Insert number
  Shift+F1~F6  Insert hex digit A~F
  + - * /      Basic operation
  BACKSPACE    Delete command
  X<>Y         Swap stack register
  LASTx        Duplicate TOS (DUP)
  CLEAR        Delete TOS (DROP)
  +/-          Negate TOS (NEG)
  E            Push 10^TOS to the stack
  Rv           Rotate (3 top stack register)
  MATH         1/X SQRT LOG LN POW SQR 10^X e^X
  TRIG         SIN COS TAN ASIN ACOS ATAN
  SUM+         Sum of range
  SUM-         Count of range
  SLOPE        SLOPE (fncell, xcell, xvalue)
  SOLVER       SOLVE (fncell, xcell, xstartvalue)
  INTEGRAL     INTEGRAL(fncell, xcell, fromvalue, tovalue)
  DEQ          DIFFERENTIAL EQUATION (fncell, xcell, ycell, tovalue)
  MATRIX       Matrix function menu
  FLAGS        Physical constants
  CUSTOM       Show cell value in grid or as stack (big numbers)

  CATALOG XEQ  Extended math menu (see below)
  PROB         Probability math menu
  COND         Conditions menu (no nesting)
  STAT STAT    Statistics menu
  CONV CONVERT Conversions menu
  MISC         Miscellaneous menu


____________________

 EXTENDED MATH MENU
____________________

When in edit mode XEQ or CATALOG (Shift +) offers an expanded math menu to
insert ie hyperbolic functions.
Please note that some functions deliver more than one result. Try to extract
the appropriate result with SWAP, CLEAR/DROP. For instance "41 C|F" yields
5 (C, Y) and 105.8 (F,  X). If you wanted to convert 41F to 5C add CLEAR/DROP
(Shift+BACKSPACE) or if you wanted to convert 41C to 105.8F add SWAP and
CLEAR/DROP to calculate on.

 HYP  Hyperbolic functions (SINH, COSH, TANH, ASINH, ACOSH, ATANH)
 PROB Probability functions (nP|Cr, LN!, P|CDF, NAND, INT)
 COND Conditions (<, =, >, IF, ELSE, THEN))
 STAT Statistics (COUNT, SUM, AVG|STDDEV, MIN|MAX, LRa|b)
 CONV Conversions (P|R, HMS|H, kg|lb, °C|°F, cm|in, l|gal))
 MISC Miscellaneous (MAT, VAL, DEQ, SLOPE, SOLVE, INTEGRAL)

Please note that VAL copies the recent value of the cell as plain value to
this cell. The recent formula of this cell will be deleted.


____________________

 EDIT MODE (TEXT)
____________________

When defining (ALPHA or STO) or editing (EDIT, ENTER/F1) a text cell all
possible characters will be shown an can be selected using the navigtion pad.
Please note that the number of characters per cell is limited to 9.

  ENTER/F1 STO Enter text and exit text mode (to navigation mode)
  INS/F2 5     Insert selected character to text
  CLR/F4       Clear complete text
  <-/F5        Edit cursor left
  ->/F6        Edit cursor right
  BSPC         Delete character
  NAVIGATE     Use navigation pad to select character


____________________

 CALCULUS
____________________

The PLOT, SLOPE, SOLVER and INTEGRAL functions evaluate a cell containing a
function (fncell) which depends itself of a referenced cell (xcell).
Additionally PLOT and INTEGRAL demand two range x-values (values only no
references).
To see the function plot navigate to the cell containing the PLOT command
(don't edit) and press PGM.FCN.
SOLVER tries to find the root of the fncell variating the xcell using Newton's
secant method. As start value SOLVER uses the value of xcell.
INTEGRAL uses the Simpson's formula and divides the range into 10 stripes.

Please note that DEQ solves a differential equation y'=f(x,y) with given
start value y(x0) due to Runge-Kutta with 4th order (RK4). As arguments DEQ
needs fncell, xcell, ycell and a x-value for the calculated y-value of the
function that solves the differential equation.


____________________

 MATRIX
____________________

In edit mode you can enter matrix functions using MATRIX or the math menu (XEQ).
A reference to a matrix references to the first matrix cell (1|1).
Please note that RACK42 deals with 3x3 matrices only - smaller matrices can be a
subset.
Matrix functions that create a new matrix write 3x3 (hard coded) values to the
spreadsheet at the target cell (to) if there is sufficient room on the
spreadsheet. Please be careful using these commands without a target cell to not
overwrite existing contents of the spreadsheet.

 DET   Determinant (from)
 TRANS Transpose (from, to)
 INV   Inverse (from, to)
 MULT  Multiply (from1, from2, to)
 SUB   Substract (from1, from2, to)
 ADD   Add (from1, from2, to)


____________________

 BAR GRAPHIC
____________________

RACK42 can display a simple bar graphic. Enter the desired text (optional) and
the  related data in two colums. Define in another cell the range of the data
column (references to first and last data cell). Navigate to this "reference
cell" and press PRINT to view a simple bar chart. As the bars are scaled the
maximum value will be printed in the first line. Please note that bars with
negative values are not printed.

Please note that RACK42 supports function plots (see chapter CALCULUS).


____________________

 SPECIFICATIONS
____________________

Spreadsheet, Calculator:
  6 15   Number of columns and rows
  3 5    Number of columns and rows to be displayed
  8      Size of calculation stack
  5      Size of stack for reference addresses
  40     Number of commands per cell
  9      Cell width; max. number of letters of text cell
  30 50  Pixel size of function plot
  100    Maximal number of iterations (solver)
  1E-8   Differential step (slope, solver)
  100    Number of stripes (integration, differential equation)

TED:
  8192   Maximal size of text files
  7      Number of displayed text lines

DRAW:
  7 28   Size of character drawing board
  30     Maximal number of drawing objects
  25     Maximal length of text objects

____________________

 PHYSICAL CONSTANTS
____________________

To enter a physical constant (2018 CODATA) press FLAGS in edit mode and the
the appropriate F-key.

 c    299792458         Speed of light
 g    9.80665           Acceleration of gravity
 G    6.67430e-11       Newton constant of gravity
 Vm   0.02271095464     Molar volume of ideal gas
 NA   6.02214076e23     Avogadro constant
 Rinf 10973731.568160   Rydberg constant
 h    6.62607015e-34    Planck constant
 Phi0 2.067833848e-15   Magnetic flux quantum
 a0   5.29177210903e-11 Bohr radius
 k    1.380649e-23      Boltzmann constant
 R    8.314462618       Molar gas constant
 F    96485.33212       Faraday constant
 t    273.15            Celsius temperature
 atm  101325            Standard atmosphere
 e    1.602176634e-19   Elementary charge
 eps0 8.8541878128e-12  Vacuum electric permittivity
 mu0  1.25663706212e-6  Vacuum magnetic permeability
 Z0   376.730313668     Impedance of vacuum
 mU   1.6605390666e-27  Atomic mass constant
 re   2.8179403262e-15  Electron radius
 me   9.1093837015e-31  Electron mass
 mp   1.67262192369e-27 Proton mass
 mn   1.67492749804e-27 Neutron mass
 mmu  1.883531627e-28   Muon mass
 muB  9.2740100783e-24  Bohr magneton
 muN  5.0507837461e-27  Nuclear magneton
 mue  -9.2847647043e-24 Electron magnetic moment
 mup  1.41060679736e-26 Proton magnetic moment
 mun  -9.6623651e-27    Neutron magnetic moment
 mumu -4.4904483e-26    Muon magnetic moment
 alph 7.2973525693e-3   Fine structure constant
 sigm 5.670374419e-8    Stefan-Boltzmann constant
 G0   7.748091729       Conductance quantum
 gamp 2.6752218744e8    Proton gyromagnetic ratio
 C1   3.741771852e-16   First radiation constant
 C2   1.438776877e-2    Second radiation constant


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
