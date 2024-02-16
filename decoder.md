# Decoder

A decoder is a combinational logic circuit that converts binary information from n input lines to a maximum of $2^n$ unique output lines. A decoder is also called a "n-to-2^n" decoder. The decoder is used to demultiplex the data from one of the many input lines to one of the many output lines. It is the opposite of the encoder.


## Full Adder using Decoder

A full adder can be implemented using a 3-to-8 line decoder. The truth table for a full adder is shown below:

$$
\begin{array}{|ccc|cc|c|}
\hline
A & B & C_{in} & S & C_{out} & Minterm \\
\hline
0 & 0 & 0 & 0 & 0 & m_0 \\
0 & 0 & 1 & 1 & 0 & m_1 \\
0 & 1 & 0 & 1 & 0 & m_2 \\
0 & 1 & 1 & 0 & 1 & m_3 \\
1 & 0 & 0 & 1 & 0 & m_4 \\
1 & 0 & 1 & 0 & 1 & m_5 \\
1 & 1 & 0 & 0 & 1 & m_6 \\
1 & 1 & 1 & 1 & 1 & m_7 \\
\hline
\end{array}
$$

The minterms for the outputs are:
$$
F_s = \sum (m_1, m_2, m_4, m_7) \\
F_{Co} = \sum (m_3, m_5, m_6, m_7)
$$
