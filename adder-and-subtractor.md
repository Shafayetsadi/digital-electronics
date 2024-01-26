# Adder & Subtractor

## Half Adder

A half adder is a combinational circuit that performs the addition of two bits and produces a sum bit and a carry bit. It has two inputs: A and B, which add two input digits, and two outputs: S and C, which are the sum and carry out.

The boolean expression for the sum bit and carry bit are:
$$
S = A \oplus B \\
C = A.B
$$

{% tabs %}
{% tab title="Half Adder" %}
|  A  |  B  |  S  |  C  |
| :-: | :-: | :-: | :-: |
|  0  |  0  |  0  |  0  |
|  0  |  1  |  1  |  0  |
|  1  |  0  |  1  |  0  |
|  1  |  1  |  0  |  1  |
{% endtab %}

{% tab title="Full Adder" %}
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
{% endtab %}
{% endtabs %}

## Full Adder

A full adder is a combinational circuit that performs the addition of three bits (two significant bits and a previous carry) and produces a sum bit and a carry bit. It has three inputs: A, B and $$C_{in}$$, which add three input digits, and two outputs: S and $$C_{out}$$, which are the sum and carry out.

In the K-Map, we see a chess board configuration.

The boolean expression for the sum bit and carry bit are:
$$
S = A \oplus B \oplus C_{in} \\
C_{out} = A.B + B.C_{in} + A.C_{in} \\
C_{out} = A.B + C_{in}.(A \oplus B)
$$

## Full Adder using Half Adder

A full adder can be implemented using two half adders and one OR gate.

## Four-bit Parallel Adder using Full Adder

A four-bit parallel adder can be implemented using four full adders.

