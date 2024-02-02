# Adder & Subtractor

## Half Adder

A half adder is a combinational circuit that performs the addition of two bits and produces a sum bit and a carry bit. It has two inputs: A and B, which add two input digits, and two outputs: S and C, which are the sum and carry out.

<figure><img src=".gitbook/assets/HalfAdder.png" alt="" width="545"><figcaption><p>Half Adder</p></figcaption></figure>

Truth Table for Half Adder:

|  A  |  B  |  S  |  C  |
| :-: | :-: | :-: | :-: |
|  0  |  0  |  0  |  0  |
|  0  |  1  |  1  |  0  |
|  1  |  0  |  1  |  0  |
|  1  |  1  |  0  |  1  |

The K-Map for the sum bit is:

<figure><img src=".gitbook/assets/halfAdderSumBit.png" alt="" width="182"><figcaption><p>K-map for sum bit</p></figcaption></figure>

The boolean expression for the sum bit is:

$$
S = A \oplus B
$$

The K-Map for the carry bit is:

<figure><img src=".gitbook/assets/halfAdderCarryBit.png" alt="" width="180"><figcaption><p>K-map for carry bit</p></figcaption></figure>

The boolean expression for the carry bit is:

$$
C = A.B
$$

Logic gate for half adder:

<figure><img src=".gitbook/assets/halfAdderLogicGate.png" alt="" width="513"><figcaption><p>Half Adder</p></figcaption></figure>

## Full Adder

A full adder is a combinational circuit that performs the addition of three bits (two significant bits and a previous carry) and produces a sum bit and a carry bit. It has three inputs: A, B and $$C_{in}$$, which add three input digits, and two outputs: S and $$C_{out}$$, which are the sum and carry out.

|  A  |  B  | C\_in |  S  | C\_out |
| :-: | :-: | :---: | :-: | :----: |
|  0  |  0  |   0   |  0  |    0   |
|  0  |  0  |   1   |  1  |    0   |
|  0  |  1  |   0   |  1  |    0   |
|  0  |  1  |   1   |  0  |    1   |
|  1  |  0  |   0   |  1  |    0   |
|  1  |  0  |   1   |  0  |    1   |
|  1  |  1  |   0   |  0  |    1   |
|  1  |  1  |   1   |  1  |    1   |

The K-map for for the sum bit is:

<figure><img src=".gitbook/assets/k-mapFullAdderSumBit.png" alt="" width="280"><figcaption><p>K-map for sum bit</p></figcaption></figure>

In the K-Map, we see a chess board configuration. We can not create any groups.

The boolean expression for the sum bit is:

$$
\begin{align*}
S &= AB'C' + A'B'C + ABC + A'BC' \\
&= A \oplus B \oplus C
\end{align*}
$$

The K-map for the carry bit is:

<div>

<figure><img src=".gitbook/assets/fullAdderCarry1.png" alt=""><figcaption><p>One way</p></figcaption></figure>

 

<figure><img src=".gitbook/assets/fullAdderCarry2.png" alt=""><figcaption><p>Another way</p></figcaption></figure>

</div>

We can see that, we have more than one group configuration for the carry bit.  Every every group configuration, we will have different boolean expression. Every one of them is right.

The boolean expression for the carry bit is:

$$
\begin{align*} 
C_{out} &= A.B + B.C_{in} + A.C_{in} \\ C_{out} &= A.B + C_{in}.(A \oplus B)
\end{align*}
$$

## Full Adder using Half Adder

A full adder can be implemented using two half adders and one OR gate.

<figure><img src=".gitbook/assets/fullAdderUsingHalfAdder.png" alt=""><figcaption><p>Full adder using half adder</p></figcaption></figure>

## Four-bit Parallel Adder using Full Adder

A four-bit parallel adder can be implemented using four full adders.

<figure><img src=".gitbook/assets/fourBitFullAdder.png" alt=""><figcaption><p>Four bit full adder</p></figcaption></figure>


## Half Subtractor

A half subtractor is a combinational circuit that performs the subtraction of two bits and produces a difference bit and a borrow bit. It has two inputs: A and B, which are the minuend and subtrahend, and two outputs: D and Bo, which are the difference and borrow out. The borrow out is used in the next stage of subtraction. 

Truth Table for half subtractor:
$$
\begin{array}{|c|c|c|c|}
\hline
\ A \ & \ B \ & \ D \ & \ B_o \ \\
\hline
0 & 0 & 0 & 0 \\
\hline
0 & 1 & 1 & 1 \\
\hline
1 & 0 & 1 & 0 \\
\hline
1 & 1 & 0 & 0 \\
\hline
\end{array}
$$

The boolean expression for the difference bit is:
$$
D = A \oplus B
$$

The boolean expression for the borrow bit is:
$$
B_o = A'.B
$$

Logic gate for half subtractor:
<figure><img src=".gitbook/assets/halfSubtractorLogicGate.png" alt="" width="513"><figcaption><p>Half subtractor</p></figcaption></figure>

## Full Subtractor

A full subtractor is a combinational circuit that performs the subtraction of three bits (two significant bits and a previous borrow) and produces a difference bit and a borrow bit. It has three inputs: A, B and $$B_{in}$$, which are the minuend, subtrahend and borrow in, and two outputs: D and $$B_{out}$$, which are the difference and borrow out. The borrow out is used in the next stage of subtraction. 

Truth Table for full subtractor:
$$
\begin{array}{|c|c|c|c|c|}
\hline
\ A \ & \ B \ & \ B_{in} \ & \ D \ & \ B_{out} \ \\
\hline
0 & 0 & 0 & 0 & 0 \\
\hline
0 & 0 & 1 & 1 & 1 \\
\hline
0 & 1 & 0 & 1 & 1 \\
\hline
0 & 1 & 1 & 0 & 1 \\
\hline
1 & 0 & 0 & 1 & 0 \\
\hline
1 & 0 & 1 & 0 & 0 \\
\hline
1 & 1 & 0 & 0 & 0 \\
\hline
1 & 1 & 1 & 1 & 1 \\
\hline
\end{array}
$$

The K-map for the difference bit is:
<figure><img src=".gitbook/assets/fullSubtractorDifferenceBit.png" alt="" width="280"><figcaption><p>K-map for difference bit</p></figcaption></figure>

The boolean expression for the difference bit is:
$$
D = A \oplus B \oplus B_{in}
$$

The K-map for the borrow bit is:
<figure><img src=".gitbook/assets/fullSubtractorBorrowBit.png" alt="" width="280"><figcaption><p>K-map for borrow bit</p></figcaption></figure>

The boolean expression for the borrow bit is:
$$
B_{out} = B.C + A'.B + A'.C
$$
