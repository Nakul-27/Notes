# Binomial Distribution 
## Requirements
- [[Binary Variable]] that is [[discrete]]
- Fixed number of attempts, $n$
- Same Probability of success on each attempt, $\pi$

## [[Probability]]
The probability that there are $k$ "successes" in $n$ attempts:
$P(x=k)={n \choose k}\pi^{k}(1-\pi)^{n-k}$
where 
${n \choose k} = \frac{n!}{k!(n-k)!}$ 

## Expected Value and [[Standard Deviation]]
$E(X) = \mu_{x} = n\pi$
$SD(X) = \sigma_{x} = \sqrt{\pi(1-\pi)}$