## Maps (functions)

Let $A$ and $B$ be sets. $A$ maps to $B$, $A \to B$. Let's write:
	- the domain A as $n$
	- the the range B as $m$

- To find the **total** number of **maps** from $A \to B$ we do: 
	$$ |m^{n}| $$
#### Given $|n| < |m|$

- Given that $|n| < |m|$ there **can't be a surjective** (onto) mapping. This is because all of the elements from the range (m)  must have a pre-image; since the domain(n) is smaller it isn't possilbe. This means that the mapping **can't be bijective** either.

- To find the **total** number of **injective maps** from $A \to B$ given $|n| \le |m|$ we do:
	$$ \frac{m!}{(m-n)!} $$

#### Given $|n| > |m|$
- Given that $|n| > |m|$ there **can't be an injective** (one to one) mapping. This is because not all of the elements from the domain(n) can connect to a distinct image/range (m) since the domain is larger. This means that the mapping **can't be bijective** either.

- To find the number of Surjective maps from $A \to B$ we do: 
	$$m^n – {m\choose 1}(m-1)^n + {m \choose 2}(m-2)^n – {m\choose 3}(m-3)^n+….- {m \choose m-1} (1)^n$$ 
##### For a **Bijective Map**
- A bijective map is needs to be (Injective) $|m| \ge |n|$ **and** (Surjective) $|n| \ge |m|$. So it is only possible if $|n| = |m|$
- To find the total number of Bijective maps from $A \to B$ we do: $n!$ 