# Eventual positivity at dilation 151/100

Assume RH and set $b=151/100$. Then $\liminf_{y\to\infty}D_b(y)/\sqrt y>3/1000$. In particular the prime sum on $(y,2.2801y)$ is eventually strictly below its main term.

Let $W_b(t)$ equal $b(1-1/t)$ for $1<t\le b$, $b^2/t-1$ for $b<t<b^2$, and zero elsewhere. Define $P_b(y)=\sum_{p\ {\rm prime}}(\log p)W_b(p/y)$ for $y>0$, with natural logarithms. Its expected main term is $b(b-1)y\log b$. Write $B_b=2\sqrt b(\sqrt b-1)^2$ for the asymptotic prime-square contribution, $D_b(y)=b(b-1)y\log b-P_b(y)$ for the deficit and $H_b(s)=(b^s-1)(b^s-b)/(s(s-1))$ for the Mellin transform.

The general extremal bound gives $\liminf D_b(y)/\sqrt y\ge B_b-L_b$ under RH, where $L_b$ is the sum of the absolute zero coefficients. At this dilation the original ramp vanishes, so the closed formula uses only logarithms, $\pi$, Euler's constant and $\sqrt b$. The executable encloses these quantities with rational endpoints and proves $B_b-L_b>3/1000$. Numerically the endpoint is about $0.00312999$. [Derivation of the general extremal formula](https://github.com/leecrossley/prime-band-extrema/tree/v1.0.0)

## Verification

The executable certifies the strict numerical inequality. The asymptotic implication uses the written explicit-formula argument. A numerical threshold for the start of permanent positivity is open here.

The recorded run used Python 3.9.6 on arm64 macOS. The verifier requires Python 3.9 or later and uses only the standard library.

```sh
bash verify-release.sh
```

The command checks the release manifest, reruns the arithmetic, and compares its output with the recorded result.

[Recorded verification output](evidence/check.txt) · [SHA-256 manifest](SHA256SUMS) · [Tagged publication](https://github.com/leecrossley/prime-band-151-100/releases/tag/v1.0.0)
