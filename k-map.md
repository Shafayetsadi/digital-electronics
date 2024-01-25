# K-Map

## Karnaugh Map

This is a method to simplify boolean algebra expressions. It reduces the need for extensive calculations by taking advantages of human's pattern recognition capability.

The required boolean results are transferred from a truth table onto a two-dimensional grid where the cells are ordered in Gray Code, and each cell position represents one combination of input conditions, while each cell value represents the corresponding output value. Optimal groups of 1s or 0s are identified. These terms can be used to write a minimal boolean expression representing the required logic.

## Rules of Simplification

* Adjacent cell on a K-Map differs by only one variable.
* Groups may not include any cell containing a zero.
* Groups maybe horizontal or vertical, but not diagonal.
* Group must contain $$2^n$$cells, like 1, 2, 4, or 8.
* Groups should be as large as possible.
* Each cell containing a 1 must be in at least one group.
* Groups may overlap
* Groups may wrap around the table. Like the leftmost cell in a row may be grouped with the rightmost cell in that row. Similar for columns also.
* Number of groups should be as few as possible.

## Example

Canonical SOP:

$$
F = \bar A B \bar C + A \bar B \bar C + A \bar B C + A B \bar C + A B C \\ F = \bar A B \bar C + A \bar B ( \bar C + C ) + A B ( C + \bar C) \\ F = \bar A B \bar C + A \bar B + A B \\ F = \bar A B \bar C + A F= A + B \bar C
$$

<table data-full-width="false"><thead><tr><th align="center">A</th><th align="center">B</th><th width="173" align="center">C</th><th align="center">F</th></tr></thead><tbody><tr><td align="center">0</td><td align="center">0</td><td align="center">0</td><td align="center">0</td></tr><tr><td align="center">0</td><td align="center">0</td><td align="center">1</td><td align="center">0</td></tr><tr><td align="center">0</td><td align="center">1</td><td align="center">0</td><td align="center">1</td></tr><tr><td align="center">0</td><td align="center">1</td><td align="center">1</td><td align="center">0</td></tr><tr><td align="center">1</td><td align="center">0</td><td align="center">0</td><td align="center">1</td></tr><tr><td align="center">1</td><td align="center">0</td><td align="center">1</td><td align="center">1</td></tr><tr><td align="center">1</td><td align="center">1</td><td align="center">0</td><td align="center">1</td></tr><tr><td align="center">1</td><td align="center">1</td><td align="center">1</td><td align="center">1</td></tr></tbody></table>

K-Map Diagram for the above truth table:

<figure><img src=".gitbook/assets/k-map_3_var.png" alt="" width="452"><figcaption><p>K-Map Diagram</p></figcaption></figure>

Check the change of value of variables in rows and columns for each group. The above diagram gives the following simplified expression:

$$
F = A + B \bar C
$$

This expression is the same as the one we got from the canonical SOP. We can not further simplify this expression.

## Pros ans Cons of K-Map

### Pros

* K-Map provides a visual and systematic method.
* Easy to use.

### Cons

* Effective, but only up to 5-6 input variables.
* Manual process.
* Error-prone.
