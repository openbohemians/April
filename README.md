# April

A new take on APL.

Spaces are required.

All objects are tensors.

Unicode with ASCII translation.

# Basic Math

```apl
1 + 1 = 2
2 - 1 = 1
2 • 3 = 6
6 ÷ 3 = 2

6 /\ 5 = 6
6 \/ 5 = 5
```

# Vector Math

Basic math operations applied to vectors are elementwise..

```apl
1 2 3 + 1
= 2 3 4 

1 2 3 + 1 2 3
= 2 4 6

1 2 3 × 2 
= 2 4 6

1 2 3 × 1 2 3
= 1 4 9
```

# Sequences

Simple repetitive sequence.

```apl
0 * 3 = 0 0 0

1 2 * 3 = 1 2 1 2 1 2
```

A *range* can be created with ellipses `...`, three periods in ASCII form.

```
1 ... 5 = 1 2 3 4 5
```

The second argument can be an open function, which then acts as an iterator.

 ```apl
1 ... ( • 2 ) * 3 = 2 4 8
```

```apl
 3 # 4 = 3 4 5 6
```

# Rank / Dimensions

```apl
    1 2 3 4 ° 2 = ( 1 2 ) ( 3 4 )

    1 2 | 3 4 

    1 2 | 3 4 || 5 6 | 7 8 =
    ( ( 1 2 ) ( 3 4 ) ) ( ( 5 6 ) ( 7 8 ) )
```

# Matrix Math

Transpose a vector or matrix with `™` or superscript `T`.

    1 2 × 3 4 ™ = 11

This is of course the dot or scalar product, which we can also write using a middot.

    1 2 • 3 4 = 11

# Rotation

```apl
1 2 | 3 4 () 2 
```

The rotation operator transforms the tensor such
that the second dimension, hence `2` as the operand,
becomes the first dimension.

```
1  2        3  1
       ->
3  4        4  2
```

This is a clockwise rotation. We can negate the
dimesion operand to rotate counter-clockwise.

For higher dimensional tensors, any rotational
orientation becomes possible by successive calls
of the rotation operator. But of course, we can 
simplify this by using a vector.

```apl
v () 2 3 = v () 2 () 3
```

It is important to keep in mind that even tensors
with lower rank can be oriented into higher dimensions.
The simple example is a row vector becoming a column
vector.


# Indexing

1 2 3 @ 1 = 1

1 2 3 4 ° 2 @ 2 = 3 4

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


# TEXTUAL DATA

Text is stored in trees.

    "Hello" >< "!" = "Hello!"

    "Hello" <- "l" = "Heo"

    "Hello" # "l" = 2

    "Hello" @ 1 = "H"

    
# FUNCTIONS

    *+ -> a * u + u .
