## Polygon Area Calculator

A Python library implementing object-oriented representations of Rectangles and Squares, providing calculations for geometric properties, ASCII representation rendering, and shape containment logic.

## Overview

This project provides a simple object-oriented model to work with basic 2D geometric shapes. It solves the problem of calculating geometric metrics (area, perimeter, diagonal) programmatically, rendering visual ASCII art representations of shapes, and calculating how many times a given shape can fit completely inside another.

## Features

- **Rectangle Class**: Defines a rectangle with width and height properties.
- **Square Class**: Inherits from `Rectangle` with synchronized dimensions to ensure side lengths remain equal.
- **Property Calculations**: Instant calculation of area, perimeter, and diagonal length.
- **ASCII Rendering**: Generates a string representation of the shape using `*` characters (up to 50 units in width or height).
- **Shape Containment Calculation**: Computes how many instances of another shape fit inside the current shape without rotation.

## Tech Stack

- Language: Python 3.x
- Standard Library: `math` module

##Testing 

from PolygonAreaCalculator import Rectangle, Square

# Create and measure a Rectangle
rect = Rectangle(10, 5)
print(rect.get_area())        # Output: 50
print(rect.get_perimeter())   # Output: 30
print(rect.get_diagonal())    # Output: 11.180339887498949
print(rect.get_picture())     # Outputs a 10x5 grid of '*'

# Create and adjust a Square
sq = Square(5)
sq.set_side(3)
print(sq.get_area())        # Output: 9

# Calculate how many squares fit inside a rectangle
rect.set_width(16)
rect.set_height(8)
print(rect.get_amount_inside(sq)) # Output: 10
