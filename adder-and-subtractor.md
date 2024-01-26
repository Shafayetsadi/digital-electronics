# Adder & Subtractor

## Half Adder

A half adder is a combinational circuit that performs the addition of two bits and produces a sum bit and a carry bit. It has two inputs: A and B, which add two input digits, and two outputs: S and C, which are the sum and carry out.

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

A full adder is a combinational circuit that performs the addition of three bits (two significant bits and a previous carry) and produces a sum bit and a carry bit. It has three inputs: A, B and Cin, which add three input digits, and two outputs: S and Cout, which are the sum and carry out.
