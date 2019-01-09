---
layout: project
title: Bootstrap Consensus Networks
description: Metoda stylometryczna do obrazowania podobieństw między tekstami wykorzystująca narzędzia analizy sieci.
thumbnail: network_thumbnail.jpg
permalink: /pl/projekty/analiza_sieci/
ref: networks
lang: pl
---


<div>
    <img class="col three left" src="{{ site.baseurl }}/assets/img/network.jpg" alt="" title="Wybór 124 starożytnych tekstów greckich (proza, poezja epicka i dramat) porównanych za pomocą metody Bootstrap Consensus Networks"/>
</div>
<div class="col three caption">
    Fig. 1: Wybór 124 starożytnych tekstów greckich (proza, poezja epicka i dramat) porównanych za pomocą metody Bootstrap Consensus Networks.
</div>


Stylometria – by podać możliwie najbardziej zwięzłą definicję – polega na porównywaniu policzalnych cech języka w tekstach pisanych, by wyodrębnić grupy podobnych dzieł. Bez względu na to, czy taka procedura ma na celu określenie autorstwa anonimowego testu, czy też wyodrębnienie różnch typów tekstów, podstawowy cel jest zawsze taki sam: chodzi o pogrupowanie podobnych do siebie tekstów w jednorodne grupy.

Wiele jest metod służących temu zadaniu, w tym hierarchiczna analiza skupień (Hierarchical Cluster Analysis) czy skalowanie wielowymiarowe (Multidimensional Scaling). Celem niniejszego projektu było przezwyciężenie pewnych ograniczeń tych metod; za inspirację posłużyła metodologia analizy sieci oraz techniki wielokrotnego próbkowania (tzw. bootstrap). Nazwa metody – Bootstrap Consensus Networks – nadal czeka na swój polski ekwiwalent.

Pomysł był następujący: Niech węzłami sieci będą poszczególne teksty z korpusu i niech każdy z tych tekstów zostanie połączony ze swoim najbliższym sąsiadem (tj. tekstem najbardziej podobnym stylistycznie). Tym samym dostaniemy sieć najsilniejszych podobieństw. Niestety już na pierwszy rzut oka widać, że taka sieć przejmie wszystkie ograniczenia dotychczasowych metod, np. analizy skupień. Połączenia między tekstami będą przecież trochę inne dla 100 najczęstszych słów, inne dla 200 słów itd. Jeżeli jednak dopuścimy myśl, że wyniki dla 100 słów i dla 500 słów pokazują w gruncie rzeczy tę samą rzeczywistość tekstową, ale oglądaną z różnych perspektyw, to możemy podjąć próbę ogarnięcia tej skomplikowanej struktury przez syntezę wielu jednostkowych analiz. Mówiąc obrazowo: jeśli chcemy się czegoś dowiedzieć o katedrze Notre-Dame w Rouen, nie wystarczy obejrzenie jednej fotografii. Kilka różnych ujęć od frontu i od tyłu, w różnych porach dnia, uzupełnione jakimiś sztychami z epoki oraz przede wszystkim słynnymi płótnami Claude Moneta – dopiero wielość perspektyw da nam jakieś wyobrażenie o katedrze. Choć nadal nie jest to wiedza obiektywna, to jednak mając wiele punktów odniesienia, jesteśmy w stanie oddzielić to, co powtarzalne, od tego, co akcydentalne.

Tę samą zasadę możemy zastosować w badaniu tekstów literackich. Jeśli dzarysowaną powyżej procedurę znajdowania podobieństw tekstowych powtórzymy dla różnych parametrów eksperymentu, na przykład dla 100, 200, 300, … 1000 najczęstszych słów, i zsumujemy wszystkie połączenia, które pojawiły się na poszczególnych etapach obliczeń, to efektem będzie sieć rejestrująca wszystkie jednostkowe „fotografie” stylometryczne. Oczywiście pewne połączenia będą się powtarzały, inne okażą się jednorazowe. Im częściej dane połączenie się powtórzy, tym mocniejsza będzie jego siła, co na wykresie zostanie przedstawione grubszą linią. Grubość połączenia jest więc miarą podobieństwa, a pośrednio również miarą stabilności wyników. Rys. 1 przedstawia tego typu sieć; została ona utworzona na podstawie 124 utworów starogreckich prozatorskich, epickich i dramatycznych (dobór konkretnych tekstów był dość przypadkowy).

Więcej na temat niniejszej metody znajduje się [tutaj](https://computationalstylistics.github.io/projects/bootstrap-networks/) (w języku angielskim). Pełne studium, w którym wyjaśnione zostały zarówno założenia teoretyczne, jak i implementacja:

> **Eder, M.** (2017). [Visualization in stylometry: cluster analysis using networks](http://dsh.oxfordjournals.org/content/early/2015/12/02/llc.fqv061). _Digital Scholarship in the Humanities_, **32**(1): 50–64, [[pre-print](https://github.com/computationalstylistics/preprints/blob/master/m-eder_visualization_in_stylometry.pdf)].

Podstawowe założnia metody zostały również, w postaci nieco uproszczonej, przedstawione w niniejszym artykule:

> **Eder, M.** (2014). Metody ścisłe w literaturoznawstwie i pułapki pozornego obiektywizmu – przykład stylometrii. _Teksty Drugie_, **2**: 90–105.

