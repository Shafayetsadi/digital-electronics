# Encoder

An encoder is a combinational circuit that converts binary information in the form of a 2^n input lines into n output lines, which represent n bit binary code for the input. For example, a 4-to-2 line encoder has 4 input lines and 2 output lines. The output lines generate the binary code corresponding to the input value. For a 8-to-3 line encoder, the input lines are 8 and the output lines are 3.

Encoders play a crucial role in various applications. They are commonly used in data transmission systems where they help in reducing the amount of data to be transmitted by converting it into a binary format. They are also used in data storage solutions to encode data before it is stored, ensuring efficient use of storage space.

There four types of encoders:

1. Priority Encoder
2. Decimal to BCD Encoder
3. Octal to Binary Encoder
4. Hexadecimal to Binary Encoder

## Priority Encoder

A priority encoder is a circuit that has multiple inputs and a single output. It is used to convert the highest priority input line into a binary code. The highest priority input line is the one with the highest value. The priority encoder is used in digital systems to determine the highest priority input. It is used in microprocessors to determine the highest priority interrupt.

### Block Diagram - Priority Encoder

The block diagram of a 4-to-2 line priority encoder is shown below:

<figure><img src=".gitbook/assets/encoder/priority-encoder.png" alt=""><figcaption><p>Priority Encoder</p></figcaption></figure>

In the figure, the inputs are I0, I1, I2, and I3. The outputs are Y0 and Y1. I0 is the least significant bit(lowest priority) and I3 is the most significant bit(highest priority). The output Y1 is the most significant bit and Y0 is the least significant bit.

### Truth Table

The truth table for a 4-to-2 line priority encoder is shown below:

$$
\begin{array}{|cccc|cc|}
\hline
I_3 & I_2 & I_1 & I_0 & Y_1 & Y_0 \\
\hline
0 & 0 & 0 & 0 & x & x \\
0 & 0 & 0 & 1 & 0 & 0 \\
0 & 0 & 1 & x & 0 & 1 \\
0 & 1 & x & x & 1 & 0 \\
1 & x & x & x & 1 & 1 \\
\hline
\end{array}
$$

The K-map for the output Y1 is shown below:

<figure><img src=".gitbook/assets/encoder/priority-encoder-kmap.png" alt=""><figcaption><p>K-map for Y1</p></figcaption></figure>

The boolean expression for Y1 is:
$$
Y_1 = I_2 + I_3
$$

The K-map for the output Y0 is shown below:

<figure><img src=".gitbook/assets/encoder/priority-encoder-kmap-1.png" alt=""><figcaption><p>K-map for Y0</p></figcaption></figure>

The boolean expression for Y0 is:
$$
Y_0 = I_3 + I_1I_2'
$$


### Advantages of Priority Encoder

1. It is used to encode multiple inputs into a binary code.
2. It is used to determine the highest priority input.
3. It is used in microprocessors to determine the highest priority interrupt.

### Disadvantages of Priority Encoder

1. It is complex to design and implement.
2. It requires more hardware resources.

## Decimal to BCD Encoder

A decimal to BCD encoder is a circuit that has 10 input lines and 4 output lines. It is used to convert a decimal number into a binary-coded decimal (BCD) number. The BCD number is a binary representation of a decimal number. The input lines are from 0 to 9 and the output lines are A, B, C, and D.

### Block Diagram - Decimal to BCD Encoder

The block diagram of a decimal to BCD encoder is shown below:

<figure><img src=".gitbook/assets/encoder/decimal-to-bcd-encoder.png" alt=""><figcaption><p>Decimal to BCD Encoder</p></figcaption></figure>

In the figure, the inputs are 0, 1, 2, 3, 4, 5, 6, 7, 8, and 9. The outputs are A, B, C, and D. The input 0 is the least significant bit and the input 9 is the most significant bit. The output D is the most significant bit and the output A is the least significant bit.

### Truth Table - Decimal to BCD Encoder

The truth table for a decimal to BCD encoder is shown below:

$$
\begin{array}{|c|cccc|}
\hline
Input & D & C & B & A \\
\hline
0 & 0 & 0 & 0 & 0 \\
1 & 0 & 0 & 0 & 1 \\
2 & 0 & 0 & 1 & 0 \\
3 & 0 & 0 & 1 & 1 \\
4 & 0 & 1 & 0 & 0 \\
5 & 0 & 1 & 0 & 1 \\
6 & 0 & 1 & 1 & 0 \\
7 & 0 & 1 & 1 & 1 \\
8 & 1 & 0 & 0 & 0 \\
9 & 1 & 0 & 0 & 1 \\
\hline
\end{array}
$$

$$
\begin{align*}
D &= 1, \text{ if input is 8 or 9} \\
C &= 1, \text{ if input is 4, 5, 6, 7, 8, or 9} \\
B &= 1, \text{ if input is 2, 3, 6, 7, 10, or 11} \\
A &= 1, \text{ if input is 1, 3, 5, 7, 9, 11, 13, or 15} \\
\end{align*}
$$
