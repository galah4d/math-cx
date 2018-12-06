# math - Mathematical package for CX 

This module provides access to a series of mathematical functions.

# Installation
This module requires the 0.5.18 version of [CX](https://github.com/skycoin/cx).

After installing [CX](https://github.com/skycoin/cx) and all its dependencies clone this repository to by running:

```sh
$ git clone https://github.com/galah4d/math-cx.git
```
It is probably a good idea to keep all your CX modules in once place so fell free to move the installation to wherever you see fit but make sure to remember it's location since it will be needed later.

# Importing the Module

After installing the module you must import it inside of your CX program in order to use it. This can be done by including the following import statement in your program:

```cx
import math
```
You should now have access to all functions inside the math module (a detailed explanation on how to use each on of these functions can be found bellow).

# Running your Program
Currently CX isn't able to automatically manage dependencies so we have to manually do this at compile time. In order to do so you must specify the path to the math module before your own CX files while executing the cx command. This can be achieved by doing:
```bash
cx $CXPATH/pkg/math-cx/math.cx you_file.cx
```
The previous example is only valid if you have installed the module to "$CXPATH/pkg/math-cx/". If this isn't the case you must change it to your own custom installation path.

## Number representation functions.

### math.abs(x f64)
Returns the absolute value of x.

```cx
package main
import math

func main() {
    f64.print(math.abs(-18.7D)) // Outputs 18.7
}
```

### math.inv(x f64)
Returns the inverse value of x.

```cx
package main
import math

func main() {
    f64.print(math.inv( 12.1D)) // Outputs -12.1
    f64.print(math.inv(-12.1D)) // Outputs  12.1
}
```

### math.ceil(x f64)
Returns the smallest integer value greater than or equal to x.

```cx
package main
import math

func main() {
    f64.print(math.ceil(8.1D))  // Outputs  9
    f64.print(math.ceil(8.7D))  // Outputs  9

    f64.print(math.ceil(-3.2D)) // Outputs -3
    f64.print(math.ceil(-3.8D)) // Outputs -3
}
```

### math.floor(x f64)
Returns the largest integer value less than or equal to x.

```cx
package main
import math

func main() {
    f64.print(math.floor(8.1D))  // Outputs  8
    f64.print(math.floor(8.7D))  // Outputs  8

    f64.print(math.floor(-3.2D)) // Outputs -4
    f64.print(math.floor(-3.8D)) // Outputs -4
}
```

## Power and logarithmic functions.

### math.pow(a f64, b i64)
Returns a raised to the power of b. (Note: b must be a positive integer)

```cx
package main
import math

func main() {
    f64.print(math.pow(2.0D, 4L))  // Outputs  16.0
    f64.print(math.pow(3.6D, 5L))  // Outputs  604.66176

    f64.print(math.pow(-2.0D, 2L)) // Outputs  4.0
    f64.print(math.pow(-2.0D, 3L)) // Outputs -8.0
}
```

## Angular conversion functions.

### math.degrees(x f64)
Converts the angle x from radians to degrees.

```cx
package main
import math

func main() {
    f64.print(math.degrees(math.PI))  // Outputs  180.0
}
```

### math.radians(x f64)
Converts the angle x from degrees to radians.

```cx
package main
import math

func main() {
    f64.print(math.radians(180.0D))  // Outputs 3.1415926536
}
```

## Constants.

### math.PI
The mathematical constant pi with 10 decimals precision.

```cx
package main
import math

func main() {
    f64.print(math.PI)  // Outputs  3.1415926536
}
```

### math.E
The mathematical constant e with 10 decimals precision.

```cx
package main
import math

func main() {
    f64.print(math.E)  // Outputs  2.7182818284
}
```

## Trigonometric functions.
Work in progress...

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.


## Disclamer
This module is still in alpha, functions can contain bugs.