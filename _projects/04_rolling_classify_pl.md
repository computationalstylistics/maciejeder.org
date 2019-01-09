---
layout: project
title: Rolling Stylometry
description: Metoda stylometryczna tzw. klasyfikacji nadzorowanej, w której badany tekst jest najpierw podzielony na równej długości fragmenty, a następnie przyporządkowany sekwencyjnie do zdefiniowanych klas.
thumbnail: rolling_thumbnail.jpg
permalink: /pl/projekty/rolling_stylo/
ref: rolling_stylo
lang: pl
---





<div>
    <img class="col three left" src="{{ site.baseurl }}/assets/img/rolling.jpg" alt="" title="<i>Biblia królowej Zofii</i> przebadana za pomocą metody Rolling Stylometry; użyte zostały następujące parametry: frekwencje 100 najczęstszych słów, próbki o długości 5000 wyrazów, prędkość próbkowania (czyli liczba wyrazów przy próbkowaniu “na zakładkę”) 4500 wyrazów."/>
</div>
<div class="col three caption">
    Rys. 1: <i>Biblia królowej Zofii</i> przebadana za pomocą metody Rolling Stylometry; użyte zostały następujące parametry: frekwencje 100 najczęstszych słów, próbki o długości 5000 wyrazów, prędkość próbkowania (czyli liczba powtórzonych wyrazów przy próbkowaniu “na zakładkę”) 4500 wyrazów.
</div>


Metoda Rolling Stylometry (może kiedyś doczeka się polskiej nazwy?) jest zaprojektowana do wykrywania zmian stylistycznych w dłuższych tekstach. By odwołać się do przykładu: wyobraźmy sobie tekst, który prawdopodobnie został napisany przez więcej niż jednego autora – chcielibyśmy znaleźć miejsce prawdopodobnego przejścia z jednego stylistycznego “sygnału” do drugiego. Gdyby to była _Biblia królowej Zofii_, czyli najstarszy polski przekład całości Biblii, pewnie bylibyśmy zainteresowani przetestowaniem dawnej hipotezy Urbańczyka, że dających się wyróżnić w rękopisie pięć różnych rąk pisarskich jest w istocie czymś więcej niż tylko pięcioma skrybami, być może bowiem byli oni również odpowiedzialni za poszczególne części przekładu. I rzeczywiście: spojrzenie na Rys. 1 pokazuje, że granica między pisarzami (pionowe przerywane linie) na ogół pokrywa się ze zmianą stylistyczną (przejście między kolorami na poziomym pasku). 

Ogólne założenie metodologiczne jest tu dość proste: tekst do analizy (np. anonimowy tekst, który chcemy atrybuować) zostaje pocięty na próbki równej długości, częściowo zachodzące na siebie. Dzięki temu zamiast analizować tekst jako całość, możemy wykonać test atrybucyjny dla każdego kolejnego fragmentu; efektem jest cała sekwencja “sygnałów” autorskich, ułożonych wzdłuż badanego tekstu. Powyższą ogólną koncepcję można połączyć w zasadzie z dowolnym klasyfikatorem nadzorowanym. Dotychczasowa implementacja w programie _stylo_ działa z trzema metodami: maszyny wektorów wspierających (Support Vector Machines), najbliższe skurczone centroidy (Nearest Shrunken Centroids) oraz z miarą Delta wprowadzoną przez Burrowsa. 

Więcej na temat niniejszej metody znajduje się [tutaj](https://computationalstylistics.github.io/projects/rolling-stylometry/), dokładniejszy opis z przykładami i z fragmentami kodu do wykorzystania opublikowany jest w [tym poście](https://computationalstylistics.github.io/blog/rolling_stylometry/) (oba w języku angielskim). Pełne studium, w którym wyjaśnione zostały zarówno założenia teoretyczne metody, jak i jej dostępne warianty oraz opisana implementacja:

> **Eder, M.** (2016). [Rolling stylometry](https://academic.oup.com/dsh/article/31/3/457/1745764). _Digital Scholarship in the Humanities_, **31**(3): 457–469, [[pre-print](https://github.com/computationalstylistics/preprints/blob/master/Eder_Rolling_stylometry_draft.pdf)].
