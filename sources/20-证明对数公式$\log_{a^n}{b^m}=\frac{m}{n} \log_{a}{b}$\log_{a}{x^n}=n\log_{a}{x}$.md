# 证明对数公式$\log_{a^n}{b^m}=\frac{m}{n} \log_{a}{b}$与$\log_{a}{x^n}=n\log_{a}{x}$

<hr>

# Formula 1

## Method 1

$$proof:\quad \log_{a^n}{b^m}=\frac{m}{n} \log_{a}{b}  $$
$$\\ \\ $$
$$设\log*{a^n}{b^m}=x $$
$$\\ \\$$
$$ (a^n)^x=b^m \Rightarrow a^{nx}=b^{m} $$
$$\\ \\$$  
$$ \log*{a}{b^m}=nx \Rightarrow nx=m\log*{a}{b} $$
$$\\ \\$$
$$\therefore x=\frac{m\log*{a}{b}}{n} \Rightarrow \frac{m}{n} \log\_{a}{b} $$
$$\\ \\$$

<hr>

## Method 2

$$
proof:\quad \log_{a^n}{b^m}=\frac{m}{n} \log_{a}{b}
$$

$$\\  \\$$
$$\because \quad \log_{a}{b}=\frac{\log_{c}{b}}{\log_{c}{a}} $$
$$\\ \\$$

$$
\therefore \log_{a^n}{b^m}=\frac{\ln{b^m}}{\ln{a^n}}
=\frac{m\ln{b}}{n\ln{a}}
$$

$$\\ \\$$

$$
\because \log_{a}{b}=\frac{\ln{b}}{\ln{a}}
$$

$$\\ \\$$

$$
\therefore \frac{m\ln{b}}{n\ln{a}} =
\frac{m}{n} \cdot \log_{a}{b}
= \log_{a^n}{b^m}
$$

<hr>

# Formula 2

$$proof:\quad \log_{a}{x^n}=n\log_{a}{x}$$
$$\\ \\$$
$$设\log_{a}{x}=m,\quad 即a^m=x$$
$$\\ \\$$
$$则\log_{a}{x^n} \Rightarrow \log_{a}{(a^m)^n} \Rightarrow \log_{a}{a^{mn}}$$
$$\\ \\$$
$$\because a^{m}=x,\quad \log_{a}{x}=m$$
$$\\ \\$$
$$\therefore \log_{a}{a^m}=m$$
$$\\ \\$$
$$\therefore \log_{a}{a^{mn}} \Rightarrow mn$$
$$\\ \\$$
$$\because m=\log_{a}{x}$$
$$\\ \\$$
$$ \log*{a}{a^{mn}} \Rightarrow n \times m \Rightarrow n \times \log*{a}{x}$$
$$\\ \\$$
$$\therefore \log*{a}{x^n}=n\log*{a}{x}$$
