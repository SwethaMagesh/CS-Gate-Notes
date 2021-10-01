## Error Correction:
### CRC - Cyclic Redundancy Check
- The algebraic polynomial chosen as a CRC generator should have at least the following properties-
- **Rule-01:** It should not be ***divisible by x***. This condition guarantees that all the burst errors of length equal to the length of polynomial are detected.
- **Rule-02:** It should be ***divisible by x+1***. This condition guarantees that all the burst errors affecting an odd number of bits are detected.

 ***Important Notes***- 
If the CRC generator is chosen according to the above rules, then-

>- CRC can detect **all single-bit errors**
>- CRC can detect **all double-bit errors** provided the divisor contains at least three logic 1’s.
>- CRC can detect **any odd number of errors** provided the divisor is a factor of x+1.
>- CRC can detect **all burst error** of length less than the degree of the polynomial.
>- CRC can detect most of the **larger burst errors** with a high probability.

### Single Parity Error:
>- If total number of 1’s is even and even parity is used, then receiver assumes that no error occurred.
>- If total number of 1’s is even and odd parity is used, then receiver assumes that error occurred.
>- If total number of 1’s is odd and odd parity is used, then receiver assumes that no error occurred.
>- If total number of 1’s is odd and even parity is used, then receiver assumes that error occurred.

### Cryptographic attacks
***Birthday ATTACKS: Digital signature susceptibility*** –
Digital signatures can be susceptible to birthday attack. A message m is typically signed by first computing H(m), where H is cryptographic hash function, and then using some secret key to sign H(m). Suppose Alice want to trick Bob into signing a fraudulent contract. Alice prepare a fair contract m and fraudulent one m’. She then finds a number of positions where m can be changed without changing the meaning, such as inserting commas, empty lines, one versus two spaces after a sentence, replacing synonyms etc. By combining these changes she can create a huge number of variations on m which are all fair contracts.

Similarly, Alice can also make some of these changes on m’ to take it even more closer towards m, that is H(m) = H(m’). Hence, Alice can now present the fair version m to Bob for signing. After Bob has signed, Alice takes the signature and attaches to it the fraudulent contract. This signature proves that Bob has signed the fraudulent contract.

To avoid such an attack the output of hash function should be a very long sequence of bits such that birthday attack now becomes computationally infeasible.