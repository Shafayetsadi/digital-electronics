# QM Method

## Quine-McCluskey Algorithm

Quine McCluskey minimization method, is a technique for reducing for minimizing the expression in their SOP (sum of product) or POS (product of sum) form. Also called a tabular method, this method has advantages over the K-Map method, in case the number of input variables is large.  For an input variable greater than six, the K Map method becomes more complex. For such problems, McCluskey or Tabular method has a simplified approach. The McCluskey method can be used to design complex circuits in digital systems.

* It is a tabular method
* No visualization of prime implicants
* Can be programmed and implemented in a computer

### Example 01

$$
Y(A,B,C,D) = \sum m(0, 1, 3, 7, 8, 9, 11, 15)
$$

Step 1: Write the minterms in binary form.&#x20;

Step 2: Group the minterms(and don't cares) according to the number of 1s in their binary form.&#x20;

Step 3: Compare the minterms in adjacent groups. If two minterms differ in only one bit, then they are combined to form a new group. The new group is formed by replacing the differing bit with a dash or d.&#x20;

Step 4: Repeat step 3 until no more groups can be formed.&#x20;

Step 5: The minterms in each group are combined to form a prime implicant. The prime implicants are then combined to form the essential prime implicants and the non-essential prime implicants.&#x20;

Step 6: The essential prime implicants are combined to form the minimum sum of products expression.

Step 1 & 2:

<table><thead><tr><th width="247" align="center">Group</th><th align="center">Minterm</th><th align="center">A  B  C  D</th><th>Matched</th></tr></thead><tbody><tr><td align="center">0</td><td align="center">m_0</td><td align="center">0  0  0  0</td><td>✅</td></tr><tr><td align="center">1</td><td align="center">m_1<br>m_8</td><td align="center">0  0  0  1<br>1  0  0  0</td><td>✅<br>✅</td></tr><tr><td align="center">2</td><td align="center">m_3<br>m_9</td><td align="center">0  0  1  1<br>1  0  0  1</td><td>✅<br>✅</td></tr><tr><td align="center">3</td><td align="center">m_7<br>m_11</td><td align="center">0  1  1  1<br>1  0  1  1</td><td>✅<br>✅</td></tr><tr><td align="center">4</td><td align="center">m_15</td><td align="center">1  1  1  1</td><td>✅</td></tr></tbody></table>

Step  3 & 4:

{% tabs %}
{% tab title="Table 1" %}


<table>
    <thead>
    <tr>
        <th width="115" align="center">Group</th>
        <th align="center">Matched Pairs</th>
        <th align="center">A  B  C  D</th>
        <th>Matched</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center">0</td>
            <td align="center">m_0, m_1<br>m_0, m_8</td>
            <td align="center">0  0  0  d<br>d  0  0  0</td>
            <td>✅<br>✅</td>
        </tr>
        <tr>
            <td align="center">1</td>
            <td align="center">m_1, m_3<br>m_1, m_9<br>m_8, m_9</td>
            <td align="center">0  0  d  1<br>d  0  0  1<br>1  0  0  d</td>
            <td>✅<br>✅<br>✅</td>
        </tr>
        <tr>
            <td align="center">2</td>
            <td align="center">m_3, m_7<br>m_3, m_11<br>m_9, m_11</td>
            <td align="center">0  d  1  1<br>d  0  1  1<br>1  0  d  1</td>
            <td>✅<br>✅<br>✅</td>
        </tr>
        <tr>
            <td align="center">3</td>
            <td align="center">m_7, m_15<br>m_11, m_15</td>
            <td align="center">d  1  1  1<br>1  d  1  1</td>
            <td>✅<br>✅</td>
        </tr>
    </tbody>
</table>


{% endtab %}

{% tab title="Table 2" %}
<table><thead><tr><th width="104">Group</th><th width="248" align="center">Matched Pair</th><th width="234" align="center">A  B  C  D</th><th>Prime Imp</th></tr></thead><tbody><tr><td>0</td><td align="center">m_0,m_1,  m_8,m_9<br>m_0,m_8,  m_1,m_9</td><td align="center">d  0  0  d<br>d  0  0  d</td><td>B'C'</td></tr><tr><td>1</td><td align="center">m_1,m_3,  m_9,m_11<br>m_1,m_9,  m_3,m_11</td><td align="center">d  0  d  1<br>d  0   d  1</td><td>B'C</td></tr><tr><td>3</td><td align="center">m_3,m_7,  m_11,m_15<br>m_3,m_11,  m_7,m_15</td><td align="center">d  d  1  1<br>d  d  1  1</td><td>CD</td></tr></tbody></table>
{% endtab %}
{% endtabs %}

Step 5:

We will find the single cross mark in each column and mark them. These rows are the essential prime implicants.

| Prime Implicants | Minterms Involved |                                    0  1  3  7  8  9  11  15                                    |
| :--------------: | :---------------: | :--------------------------------------------------------------------------------------------: |
|       B'C'       |     0, 1, 8, 9    | <mark style="color:orange;">x</mark>  x  3  7  <mark style="color:orange;">x</mark>  x  11  15 |
|        B'D       |    1, 3, 9, 11    |                                    0  x  x  7  8  x   x  15                                    |
|        CD        |    3, 7, 11, 15   | 0  1  x   <mark style="color:orange;">x</mark>  8  9   x  <mark style="color:orange;">x</mark> |

The boolean expression is,

$$
Y = B'C' + CD
$$
