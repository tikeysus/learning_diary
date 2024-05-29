
# Purpose 

The reason for outlining data types in C is because C is a statically typed languaged. Variables cannot be declared without first telling the compiler what type of variable it is dealing with. Also, functions or structs must inform the compiler the data type that they will return after execution. C is a low level language, it is important to consider aspects such as data types and memory allocation.

# Data Types in C

## Int 

* Takes up 4 bytes (32 bits).
* Value is represented using 2's complement. 
* To increase the range of possible values that we can represent, we can assume that the integer is unsigned and use the last bit for magnitude instead of sign. 

## Char

* A single character, mapped to a set value according to ASCII convention.
* ASCII is typically 7 bits, but most implementations have extended it to 8, makes more sense given that 8 constitutes a byte. 

## Float 

* Used to represent real numbers (whole number and fraction part). 
* Different conventions for how many bits are allocated for mantissa, significand, and exponent. 
	* This is a low level concept that is covered in computer organization. Mainly depends on the convention that is used (i.e. IEEE). 

## Double 

* Represents real numbers but allocates twice as much memory, 8 bytes. 

## Void 

* Not a data type.
* This is a placeholder for "nothing" in C. 