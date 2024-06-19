# Maths for Computation Cheat Sheet
---
### Link: 
 > #CM12006 
 > #CheatSheet 
 > [[CM12006 Mathematics of Computation]]

---

1. **==Taylor series==** used to approximate function by creating **infinite polynomial** 
    - $$f(x) = \sum_{0 \leq n \leq \infty} {{(x - a)^nf^n(a)}\over{n!} }$$
    - However where $x_{new} = x + a$
        - $f(x + a) = f(a) + {{(x)f'(a)}\over{1!}} + { {x^2f''(a)}\over{2!} } + ... + {{x^nf^n(a)}\over{n!} }$
2. **==Maclurin series==** is a **rip off** of **Taylor** where $a = 0$ 
    - Equation $f(x) = f(0) + xf'(0) + { {x^2f''(0)}\over{2!} } + ... + {{x^nf^n(0)}\over{n!} }$
3. **$\delta/\epsilon$ ==Method for Continuity==**
    - **for** $∣x−c∣<δ$ **prove** $∣f(x)−f(c)∣<ϵ$
    - **Notation**: $∀ϵ>0,∃δ>0,∣x−c∣<δ⟹∣f(x)−f(c)∣<ϵ$
4. **==Vector Span==**
    - **Definition**: Span of $\{v1​,v2​,...,vk​\}$ is all combinations $a1​v1​+a2​v2​+...+ak​vk​$.
    - Make Matrix, **TRANSPOSE** the n **REDUCE** before solving 
5. **==Eigen==**
    - **Eigenval**: Solve $det(A−\lambda I)=0$
    - **Eigenvec**: Solve for $v$ $(A -\lambda I)v=0$
6. **==RSA Cryptosystem==**
    - Key Generation: $n=pq,ϕ(n)=(p−1)(q−1),e s.t. gcd(e,ϕ(n))=1,d=e−1modϕ(n)$
    - **Encryption/Decryption**: $c=m^e\mod n$  ,  $m=c^d\mod n$
7. ==**Euler's Totient Function**==
    - **For Primes**: $ϕ(p)=p−1$ , $ϕ(pq)=(p−1)(q−1)$ for $p,q$ primes

---
