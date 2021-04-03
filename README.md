# April

A new take on APL.

Spaces are required.

All objects are tensors.

Unicode with ASCII translation.

Basic Math

    1 + 1 = 2
    2 - 1 = 1
    2 × 3 = 6
    6 ÷ 3 = 2

    6 '-' 5 = 6
    6 .-. 5 = 5

Vector Math

    1 2 3 + 1 = 2 3 4 

    1 2 3 + 1 2 3 = 2 4 6

Range

    1 ... 5 = 1 2 3 4 5

    3 # 4 = 3 4 5 6

# Rank

    1 2 3 4 ° 2 = ( 1 2 ) ( 3 4 )

# Matrix Math

    1 2 ™ × 3 4 = ( 3 6 ) ( 4 8 )

# Indexing

    1 2 3 @ 1 = 1

    1 2 3 4 ° 2 @ 2 1 = 3

# Iteratives

    3 2 1 ] - = 0

    2 3 6 [ - =  1

    3 ][ * 2 . # 4 = 48

# Boolean Logic

    O (+) 0 = 0
    1 (+) 0 = 1
    0 (+) 1 = 1
    1 (+) 1 = 1

    0 (×) 0 = 0
    1 (×) 0 = 0
    0 (×) 1 = 0
    1 (×) 1 = 1

    0 (^) 0 = 0
    1 (^) 0 = 1
    0 (^) 1 = 1
    1 (^) 1 = 0

Regular numbers admit to boolean logic as well thru their binary representation.

    14 (+) 1 = 15
    14 (×) 1 = 0

# Control Flow

TODO: How to do if and if-else?

    0 { 2 = 0
    1 { 2 = 2

# Derivatives and Integrals

    ( x ^ 2 ) ' x = ( 2 × x )

    ( 2 × x ) | x = ( x ^ 2 )

# Statistics ?

    ( x | 1 ) + ( y | 0 ) = x
