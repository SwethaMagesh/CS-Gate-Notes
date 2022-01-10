## Master's Theorem

T(n) = aT(n/b) + f(n)

where, T(n) has the following asymptotic bounds:
1. If f(n) = O(n<sup>log<sub>b</sub> a-ϵ</sup>), then T(n) = Θ(n<sup>log<sub>b</sub> a</sup>).
2. If f(n) = Θ(n<sup>log<sub>b</sub> a</sup>), then T(n) = Θ(n<sup>log<sub>b</sub> a</sup> * log n).
3. If f(n) = Ω(n<sup>log<sub>b</sub> a+ϵ</sup>), then T(n) = Θ(f(n)).

ϵ &gt; 0 is a constant.

---

![image](https://user-images.githubusercontent.com/43994542/106783732-9b6ece80-6671-11eb-8803-688a9a569da7.png)
