# SOP & POS

## Sum of Products

Total number of combination = 2^n, where n is the number of variables.&#x20;

Truth Table:

<table data-full-width="false"><thead><tr><th align="center">m</th><th align="center">A</th><th align="center">B</th><th align="center">C</th><th align="center">F</th></tr></thead><tbody><tr><td align="center">0</td><td align="center">0</td><td align="center">0</td><td align="center">0</td><td align="center">0</td></tr><tr><td align="center">1</td><td align="center">0</td><td align="center">0</td><td align="center">1</td><td align="center">0</td></tr><tr><td align="center">2</td><td align="center">0</td><td align="center">1</td><td align="center">0</td><td align="center">1</td></tr><tr><td align="center">3</td><td align="center">0</td><td align="center">1</td><td align="center">1</td><td align="center">0</td></tr><tr><td align="center">4</td><td align="center">1</td><td align="center">0</td><td align="center">0</td><td align="center">1</td></tr><tr><td align="center">5</td><td align="center">1</td><td align="center">0</td><td align="center">1</td><td align="center">1</td></tr><tr><td align="center">6</td><td align="center">1</td><td align="center">1</td><td align="center">0</td><td align="center">1</td></tr><tr><td align="center">7</td><td align="center">1</td><td align="center">1</td><td align="center">1</td><td align="center">1</td></tr></tbody></table>

Boolean Function of SOP,&#x20;

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

This is known as standard or canonical SOP form. Because it is written directly from a truth table.

### Minterm

$$
F(A,B,C)=m_2+m_4+m_5+m_6+m_7 \\
F(A,B,C)=\sum(2, 4, 5, 6, 7)
$$



Product of Sums
