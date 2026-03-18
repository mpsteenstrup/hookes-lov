# system med dæmpning

Vi vil simulere et system som svingen med en dæmpning som er proportional med farten i anden, hvilket svarer til en luftmodstand. Simuleringen er den sammen som ved lodret bevægelse men nu er kraften ændret så den er
$$
F = F_{fjeder}+F_{tyngde}+F_{dæmpning}
$$

Dæmpningen bliver tilføjet med ```-d*v*abs(v)``` hvor ```v*abs(v)``` sørger for at kraften altid er modsatrettet bevægelsen, altså dæmpning.

<iframe src='https://trinket.io/embed/glowscript/9483b4b19a?toggleCode=true' width='100%' height='400' frameborder='0' marginwidth='0' marginheight='0' allowfullscreen></iframe>

Øvelse
* Kør programmet. 
* Lav ```d``` større og beskriv bevægelsen.
* Lav ```d``` negativ, hvad sker der så?



## Periodisk påvirket system
En udvidelse af simuleringen er at simulere et drevet pendul, hvor vi tilføjer en periodisk kraft. 