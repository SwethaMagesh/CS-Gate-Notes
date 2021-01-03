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