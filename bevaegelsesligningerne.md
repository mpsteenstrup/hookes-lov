## Indholdsfortegnelse
* [Horisontal bevægelse](https://mpsteenstrup.github.io/hookes-lov/horisontal-bevaegelse.html)
* [Vertikal position](https://mpsteenstrup.github.io/hookes-lov/vertikal-bevaegelse-position.html)
* [Vertikal energi](https://mpsteenstrup.github.io/hookes-lov/vertikal-bevaegelse-energi.html)
* [System med dæmpning](https://mpsteenstrup.github.io/hookes-lov/daempning.html)
* [Bevægelsesligningerne](https://mpsteenstrup.github.io/hookes-lov/bevaegelsesligningerne.html)

# Bevægelsesligningerne - udledning
Vi ved fra Newtons 2. lov at en resulterende kraft forskellig fra nul giver en acceleration. Hvis vi bruger Newtons 2. lov på Hooks lov får vi

$$
\begin{align}
F_{res} &= F_{hook} \\
m\cdot a &= -k\cdot x \\
a &= -\frac{k}{m}\cdot x.
\end{align}
$$

Vi kan opskrive accelerationene som den tidsafledte af hastigheden og hastigheden, v som den tidsafledte af stedet, x. Det giver en 1. og 2. ordens differentialligning, hvilket generelt er svære at løse.

$$
a=v'=x'' = -\frac{k}{m}\cdot x.
$$

Vi ved at en harmonisk bevægelse kan beskrives med en sinusfunktion. Det kan vises mere generelt men her bruger vi formen

$$
x(t) = A\cdot sin(\omega \cdot t),
$$

hvor *A* er svingningens amplitude og $\( \omega \)$ er vinkelhastigheden og *t* er tiden.
Vi kan nu bruge vores viden fra differentialregning til at finde hastigheden og accelerationen. Vi differentierer mht. tiden én gang,

$$
v(t) = x'(t) = A\cdot \omega\cdot cos(\omega \cdot t),
$$

og en gang til,

$$
a = v'(t) = - A\cdot \omega^2 sin(\omega \cdot t ).
$$

Nu har vi to udtryk for accelerationen, *a*, og kan sætte dem lig hinanden. Derved får vi,

$$ a = -\frac{k}{m}\cdot x =  -\frac{k}{m}\cdot A\cdot sin(\omega \cdot t)  = - A\cdot \omega^2 sin(\omega \cdot t ).
$$

Ved at isolere fjedderkonstanten, *k* , giver det

$$ k = \omega^2 \cdot m, $$

eller vinkelfrekvensen

$$ \omega = \sqrt{k/m}.$$

Vi kan nu skrive bevægelsesligningerne ned for loddet.

$$ 
\begin{align}
a(t) &= A\cdot sin(\sqrt{k/m}\cdot t)\\
 v(t) &= A\cdot\sqrt{k/m}\cdot  cos(\sqrt{k/m}\cdot t)\\
 x(t) &= -A\cdot k/m \cdot sin(\sqrt{k/m}\cdot t)
 \end{align}
 $$

```python.run
min_graf = graph(title="Sinus plot", xtitle="t", ytitle="sin(5t)", fast=False)
kurve = gcurve(color=color.blue)
t = 0
while t < 5:
    kurve.plot(t, sin(5*t))
    t = t + 0.02
```
[https://glowscript.org/#/user/mps/folder/hookeslov/program/bevaegelsesligningerne](https://glowscript.org/#/user/mps/folder/hookeslov/program/bevaegelsesligningerne)
