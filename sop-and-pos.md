# SOP & POS

## Sum of Products

It is used when the output is high.
Total number of combination = 2^n, where n is the number of variables.&#x20;

Truth Table:

<table data-full-width="false"><thead><tr><th align="center">m</th><th align="center">A</th><th align="center">B</th><th align="center">C</th><th align="center">F</th></tr></thead><tbody><tr><td align="center">0</td><td align="center">0</td><td align="center">0</td><td align="center">0</td><td align="center">0</td></tr><tr><td align="center">1</td><td align="center">0</td><td align="center">0</td><td align="center">1</td><td align="center">0</td></tr><tr><td align="center">2</td><td align="center">0</td><td align="center">1</td><td align="center">0</td><td align="center">1</td></tr><tr><td align="center">3</td><td align="center">0</td><td align="center">1</td><td align="center">1</td><td align="center">0</td></tr><tr><td align="center">4</td><td align="center">1</td><td align="center">0</td><td align="center">0</td><td align="center">1</td></tr><tr><td align="center">5</td><td align="center">1</td><td align="center">0</td><td align="center">1</td><td align="center">1</td></tr><tr><td align="center">6</td><td align="center">1</td><td align="center">1</td><td align="center">0</td><td align="center">1</td></tr><tr><td align="center">7</td><td align="center">1</td><td align="center">1</td><td align="center">1</td><td align="center">1</td></tr></tbody></table>

Boolean Function of SOP,&#x20;

$$
\begin{align*}
    F   &= A'.B.C' + A.B'.C' + A.B'.C + A.B.C' + A.B.C \\
\end{align*}
$$
In SOP form, _0 -> A', 1 -> A_.
This is known as standard or canonical SOP form. Because it is written directly from a truth table. In this form, each minterm has all the variables of the function in normal or complemented form.

$$
\begin{align*}
    F   &= A'.B.C' + A.B'.C' + A.B'.C + A.B.C' + A.B.C \\
        &= A'.B.C' + A.B'(C'+C) + A.B(C'+C) \\
        &= A'.B.C' + A.B' + A.B \\
        &= A'.B.C' + A(B'+B) \\
        &= A'.B.C' + A \\
        &= A'.B.C' + A.(B'+B) \\
        &= A'.B.C' + A \\
        &= A + B.C' \\
\end{align*}
$$

This is known as the minimal SOP form. Because it is written in the simplest form. In this form, each minterm does not have all the variables of the function in normal or complemented form.

### Minterm

$$
F(A,B,C)=m_2+m_4+m_5+m_6+m_7 \\
F(A,B,C)=\sum(2, 4, 5, 6, 7)
$$



## Product of Sums

It is used when the output is low.

Truth Table:

<table data-full-width="false"><thead><tr><th align="center">m</th><th align="center">A</th><th align="center">B</th><th align="center">C</th><th align="center">F</th></tr></thead><tbody><tr><td align="center">0</td><td align="center">0</td><td align="center">0</td><td align="center">0</td><td align="center">0</td></tr><tr><td align="center">1</td><td align="center">0</td><td align="center">0</td><td align="center">1</td><td align="center">0</td></tr><tr><td align="center">2</td><td align="center">0</td><td align="center">1</td><td align="center">0</td><td align="center">1</td></tr><tr><td align="center">3</td><td align="center">0</td><td align="center">1</td><td align="center">1</td><td align="center">0</td></tr><tr><td align="center">4</td><td align="center">1</td><td align="center">0</td><td align="center">0</td><td align="center">1</td></tr><tr><td align="center">5</td><td align="center">1</td><td align="center">0</td><td align="center">1</td><td align="center">1</td></tr><tr><td align="center">6</td><td align="center">1</td><td align="center">1</td><td align="center">0</td><td align="center">1</td></tr><tr><td align="center">7</td><td align="center">1</td><td align="center">1</td><td align="center">1</td><td align="center">1</td></tr></tbody></table>

Boolean Function of POS,&#x20;
$$
\begin{align*}
    Y = (A+B+C).(A+B+C').(A+B'+C).(A+B'+C') \\
\end{align*}
$$
In POS form, _0 -> A, 1 -> A'_. This is known as standard or canonical POS form. Because it is written directly from a truth table. In this form, each maxterm has all the variables of the function in normal or complemented form.

Relation between SOP and POS:

