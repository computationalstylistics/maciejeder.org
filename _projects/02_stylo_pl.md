---
layout: project
title: Stylo
description: Oprogramowanie do analiz w zakresie stylistyki komputerowej, atrybucji autorskiej itd.
thumbnail: clustering_thumbnail.jpg
permalink: /pl/projekty/stylo/
ref: stylo
lang: pl
---


<div>
    <img class="col three left" src="{{ site.baseurl }}/assets/img/clustering.jpg" alt="" title="Analiza skupień 66 angielskich powieści od Jane Austen do Josepha Conrada: przykład zastosowania pakietu ‘stylo’"/>
</div>
<div class="col three caption">
    Rys. 1: Analiza skupień 66 angielskich powieści od Jane Austen do Josepha Conrada: przykład zastosowania pakietu ‘stylo’.
</div>

Nieuchwytne dla indeksów cytowań i innych wskazników bibliometrycznych, napisane przeze mnie programy są instalowane i używane z pewnością znacznie częściej, niż czytywane są moje rozprawy naukowe. Dotyczy to z pewnością pakietu “stylo”.

Oprogramowanie “Stylometry with R” (czy po prostu “stylo”) to uniwersalna biblioteka programistyczna napisana w języku R, a zarazem gotowy program (zestaw wysokopoziomowych funkcji) do przeprowadzania analiz stylometrycznych tekstów pisanych. Stylometria, czy też stylistyka komputerowa, zajmuje się analizą kwantytatywną stylu pisanego, w tym weryfikacją autorską, która miewa zastosowanie w wymiarze sprawiedliwości, ale przede wszystkim w badaniach nad językiem i stylem dzieł literackich. Ponieważ “stylo” oferuje łatwy w użyciu interfejs graficzny do przeprowadzania prostych analiz wysokiego poziomu, znakomicie nadaje się jako narzędzie dla początkujących użytkowników, nie mających styczności z językami programowania (szczególnie chętnie jest więc wykorzystywany w humanistyce cyfrowej). Bardziej doświadczeni jednak użytkownicy mogą wykorzystać zawarte w pakiecie funkcje niższego poziomu, by z nich konstruować własne klasyfikatory lub projektować najbardziej nawet wymagające eksperymenty z użyciem przeróżnych miar podobieństwa.

Do najczęściej wykorzystywanych i najbardziej znanych funkcjonalności pakiety “stylo” należą:

* Hierarchiczna Analiza Skupień (zob. przykładowy wykres na Rys. 1)
* Analiza Głównych Składowych
* Skalowanie Wielowymiarowe
* [Bootstrap Consensus Networks]({{ site.baseurl }}/pl/projekty/analiza_sieci/)
* Delta Burrowsa
* Maszyny Wektorów Wspierających
* Najbliższe Skurczone Centroidy
* [Rolling Stylometry]({{ site.baseurl }}/pl/projekty/rolling_stylo/)



**Autorzy:** Maciej Eder<sup>*</sup>, Mike Kestemont, Jan Rybicki, Steffen Pielström

**Licencja:** [GPL-3](https://opensource.org/licenses/GPL-3.0)

Bieżąca oficjalna wersja pakietu: 
[![CRAN Version](http://www.r-pkg.org/badges/version/stylo)](https://CRAN.R-project.org/package=stylo)

Instrukcja instalacji oraz dokumentacja użycia pakietu znajduje się na [repozytorium GitHub](https://github.com/computationalstylistics/stylo). Proszę jednak rzucić czasem okiem na podstronę [teaching]({{ site.baseurl }}/teaching/) niniejszej witryny, gdzie będę zamieszczać sukcesywnie pojawiające się dokumenty na temat pakietu.

