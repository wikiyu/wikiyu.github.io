---
layout: post
title:  "GitHub Pages prosto!"
---

# Początek

GitHub Pages to patent GitHuba by używając jekylla i paru innych OpenSource`owych projektów zrobić z repozytorium kodu normalną stronę WWW. Patent przedni. wykonanie... może kiedyś będzie lepsze. Na chwilę obecną co potrzeba wiedzieć?
Hostowanie za free, tak samo darmowe jest podpięcie swojej domeny i są dostępne szablony... Prawie jak WordPress ;-) Tyle że nie ma takiego fancy panelu admina, a i trzeba ogarniać podstawy Gita by to działało. No i jeszcze markdown czyli język znaczników. A i ... dużo czytać trzeba by poradzić sobie z rzeczami o których nikt, nigdzie, nie napisał, nigdy.

# First Step

Tworzymy repozytorium nowe, o nazwie takiej jak profil. Jak coś podejrzyjcie u mnie na https:/wikiyu.github.com jak to wygląda. Potem w panelu ustawień repozytorium ustawiacie że chcecie korzystać z Pages i już... prawie.
https://pages.github.com/ - po przejściu przez te kroki niby wszystko działa. Niby. Bo jak stworzymy nowy wpis w katalogu /_posts/ np /_posts/2018-10-26-PostTitle.md to nic się nie stanie gdyż na 99% macie szablon który domyślnie nie obsługuje postów... by obsługiwał potrzebujecie szablonu tegoż typu wpisów. Dlatego na początek polecam "minima" ale nie to minima z wyboru przez stronę tylko wpisać w _config.yml po prostu w theme: minima
Ma posty, można zrobić prostego bloga, a potem się martwić. ;-)

# Second step

Działa? To rozejrzyj się za szablonem który użyjesz lub sforkujesz i dopasujesz do siebie [ołpen sors bjacz!], łatwo to zrobić przez wpisanie w Goo... wyszukiwarkę "GitHub Pages theme jekyll". Problemem może być nadmiar takich szablonów do przejrzenia, ale dasz sobie radę. Potem polecam zrobić fork takiego repo, a dopiero z niego kopiować pliki do siebie. Tak by zawsze mieć pod ręką kopie jakbyśmy coś zepsuli i po to by móc łatwo robić update`y szablonu zmodyfikowanego przez siebie po tym jak autor oryginału też coś zmieni. Po prostu ściągamy wtedy jego zmiany z oryginalnego repo, łączymy ze swoim tak by nie popsuć i dopiero nakładamy na swój blog / na produkcję. Działa. 
# Third step

Co bardziej zapaleni nie lubią robić online... więc próbują offline psuć sobie wszystko. Toteż NIE RADZĘ na windowsie instalować wszystkiego tak by jekyll działał i kompilował nam te wszystkie ładne markdowny do html by można było podejrzeć to lokalnie. Zamiast tego polecam albo Dockera i pakiet jekyllowy tam dostępny, albo po prostu googlnąć za całą maszyną wirtualną ze wszystkim przygotowanym specjalnie dla nas, skonfigurowanym... tylko wrzucamy kopię swojego repo, tam się bawimy, jak wypluwany wynik nam pasuje to na świat i już. 

# Last step into dakrness

Edytory pod .md ... long story short - są dostępne takie online jak Dillinger, ja piszę po prostu w VSCode albo Atom zależnie od komputera... podświetlają trochę składnię, a nie muszę widzieć tego jak to się zrenderuje. No ale wygląd mnie akurat mało obchodzi tutaj. Dillinger pokazuje na bieżąco to co piszemy w formie takiej jak będzie na wyjściu. Pytanie czy ktoś myśli o używaniu GitHub Pages do jakiś dziwnych widoków niestandardowych, ale wiadomo, że co człowiek to potrzeba. 
Aha i można też zamiast markdown wrzucać teksty wprost w html... jak ktos potrzebuje. 
Have Fun!