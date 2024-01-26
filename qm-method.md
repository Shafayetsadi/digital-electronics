# QM Method

## Quine-McCluskey Algorithm

* It is a tabular method
* No visualization of prime implicants
* Can be programmed and implemented in a computer

### Example 01

$$
Y(A,B,C,D) = \sum m(0, 1, 3, 7, 8, 9, 11, 15)
$$
Step 1: Write the minterms in binary form. 
Step 2: Group the minterms(and don't cares) according to the number of 1s in their binary form.
Step 3: Compare the minterms in adjacent groups. If two minterms differ in only one bit, then they are combined to form a new group. The new group is formed by replacing the differing bit with a dash or d.
Step 4: Repeat step 3 until no more groups can be formed.
Step 5: The minterms in each group are combined to form a prime implicant. The prime implicants are then combined to form the essential prime implicants and the non-essential prime implicants.
Step 6: The essential prime implicants are combined to form the minimum sum of products expression.


