# FloatMathGB
Floating Point Arithmetic for GameBoy

Hi, this is a debugged version of float point arithmetic for GameBoy, originally published by Jeff Frohwein

I have added CALCULATOR.gb rom. This is a calcuculator (to be runned on a gameboy or a gameboy emulator)
that I created and used to test the arithmetic functions

enjoy !




Tomi



_____________________________________________________________________
BUTTON INPUTS:

U,D,L,R : 		move cursor
A button :		input
B button :		toggles primary / secondary keys on screen

A+B+SELECT+START:	reset prog

START :			return from error screens



_____________________________________________________________________
ON-SCREEN KEYS:

°/Rd :			It specifies what do you want to feed
			trigonometric functions with. (° or rad)
			(It is NOT a conversion tool)

+/-			changes the sign of the mantissa
			or the exponent part (if any) of manually
			entered values.
			If exp part already entered and you want to
			change the sign of mantissa, you must delete
			exp part first, then change mantissa sign.
			(then input exp part again)
			For a previously computed result, only the
			mantissa sign can be changed.

all the other keys are quite obvious

_____________________________________________________________________
INPUT SEQUENCE BEHAVIOR:

Similar to most of the cheap pocket calculators' behavior:


*
when hitting "=" several times it computes previous result with
previously entered binary operator along with its second parameter

example:
	input sequence:		"5" "+" "3" "=" "=" "="
	outputs:		"8" "11" "14"

**
when computing an unary operator, previously entered binary operator
(that has not been processed yet) and its first parameter
are kept in memory for further processing

examples:
	input sequence:		"5" "+" "9" "sqrt" "="
	outputs:		"3" "8"

	input sequence:		"5" "+" "9" "sqrt" "+" "4"
	outputs:		"3" "8" "12"


_____________________________________________________________________
STOP MODE:

Enters into STOP MODE after 1 minute
