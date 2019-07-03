---
title: EventStorming - co to takiego?
date: 2019-02-21
author: Krzysztof Owsiany
layout: post
tags:
  - EventStorming
comments: true
permalink: eventstorming-co-to-takiego
published: true
image: /assets/images/2019/02/eventstorming/co-to-takiego/post.png
image_big: /assets/images/2019/02/eventstorming/co-to-takiego/post-big.png
categories:
  - EventStorming
short: Coraz szerzej, więcej słyszymy o <b class='event-color'>Event</b><b class='command-color'>Storming</b>-u. Czym tak naprawdę jest ta technika? W dzisiejszym poście postaram się odpowiedzieć na to pytanie. Chciałbym też byście otworzyli umysł i zauroczyli się tą techniką. Gdyż jest bardzo wartościowa!! Zapraszam do świata zdarzeń.
---
![EventStorming - co to takiego?!][post-big]
Człowiek zazwyczaj boryka się wieloma problemami. Ciągły rozwój technologiczny wymusza na naszym gatunku równoległy rozwój intelektualny. Tworzymy coraz to bardziej zaawansowane urządzenia/oprogramowanie. Wymyślamy sposoby budowania jak najbardziej odzwierciedlające  istotę problemu. 

Jesteśmy jenak istotami ludzkimi, popełniamy błędy. To jest element naszego życia. Nie inaczej jest w przypadku powoływania do życia ambitnych idei.
Kilkukrotnie stawałem przed takim problemem, czasem się udawały. Innym razem stawiały mnie na krawędzi załamania nerwowego. A wszystko to wynika z faktu, że nie jesteśmy jasnowidzami, nie wszystko jesteśmy w stanie przewidzieć (choć wiele próbujemy).

Przez taką sytuację nie kończymy projektów, projektujemy je bardzo źle, następnie znikamy w niewyjaśnionych okolicznościach następnie pojawiając się w innej firmie;). Zostawiamy problemy za sobą. 
Czy można tego uniknąć, zapewne nie wszystkiego ale można wdrażać mechanizmy niwelujące takie sytuacje.

## Wszechświat pełen zdarzeń
[![EventStorming - co to takiego?!][image1]][image1-big]{:.post-left-image}
Jeżeli głębiej się zastanowić, to nasz wszechświat składa się ze zdarzeń i reakcji na nie. Wyzwalają one działanie innych aspektów życia. Mógłbym subiektywnie stwierdzić, że to one kontrolują wszystko. To taka reakcja łańcuchowa, najpierw wzbudzone zostaje pierwsze zdarzenie. Kolejne są skutkiem pierwszego, a dokładniej sprawę ujmując akcją jaką podejmujemy reagując na zaistniałe zdarzenie.

Przykładem tutaj może być prosta sprawa. Jazda samochodem:

**Wsiadłem do samochodu**{:.event-color} -> 
**Zapinam pas**{:.command-color} ->
**Zapiąłem pas**{:.event-color} -> 
**Przekręcam kluczyk**{:.command-color} ->
**Inicjowanie gotowości samochodu do odpalenia**{:.external-system-color} ->
**Samochód gotowy do odpalenia**{:.event-color}  -> 
**Kluczyki przekręcone na zapłon**{:.command-color} ->
**Odpalanie**{:.external-system-color} ->
**Samochód zapalił**{:.event-color} -> 
**Włączam światła**{:.command-color} ->
**Światła włączone**{:.event-color} -> 
**Wybieram bieg**{:.command-color} ->
itd.

By wykonać taką czynność, musi nastąpić wiele zdarzeń oraz reakcji na nie. To bardzo skomplikowana sekwencja.

Wygląda to mniej więcej tak: **Zdarzenie**{:.event-color}} - **reakcja**{:.command-color} - **zdarzenie**{:.event-color}} - **reakcja**{:.command-color} - **zdarzenie**{:.event-color}} - **reakcja**...

Można podejść do każdego aspektu, życia i zaobserwować występowanie różnych zdarzeń oraz innych elementów składowych pozwalających na ułożenie procesu danej czynności lub sytuacji.

## Wydarzył się - przełom
![EventStorming - co to takiego?!][event]{:.post-right-small-image}
Skoro zdarzenia są tak bardzo ważne to może warto było by zrobić z tego użytek, odpowiednio opakować wzbogacić i stworzyć sposób na opisywanie procesów jakie występują w pobliżu nas.

Tutaj wkracza **[Alberto Brandolini]** z przepisem na pizze ;).
Przedstawił światu swój autorski sposób na opisywanie procesów  o nazwie **Event**{:.event-color}**Storming**{:.command-color}. 

Opracował On technikę modelowania wszystkiego :) przy pomocy banalnych post-it-ów. 
W prostocie siła i tak właśnie można powiedzieć o **Event**{:.event-color}**Storming**{:.command-color}-u. Jest to potężne narzędzie.

**Event**{:.event-color}**Storming**{:.command-color} pozwala nam wykonać wiele przejść przez model w różnym kontekście:
* Eksploracja nieznanych obszarów,
* Szukanie problematycznych miejsc.
* Dzielenie się wiedzą.
* Modelowanie bieżącego procesu - odkrywanie jak naprawdę coś działa:).

Dla mnie osobiście to swego rodzaju podróż w przyszłość. Będą w chwili obecnej + kilka h. Można stworzyć prototyp aplikacji i zobaczyć jak będzie się  zachowywała. A co ważniejsze zweryfikować pewne ścieżki i przy pomocy mazaka i karteczki szybko i tanio zmienić decyzję.

W procesie projektowania gier stosuje się technikę o nazwie **Paper Prototyping** gdzie przy pomocy papieru i innych biurowych narzędzi przygotowujemy grę w kilka godzin. Następnie gramy w tą grę, tak jest to takie sztuczne ale pozwala na sprawdzenie pewnych projektowych założeń. Na tej podstawie można podjąć już jakieś decyzje usprawniające i zaoszczędzić dużo **$**. Technika jest także stosowana w innych dziedzinach np.: [projektowaniu interfejsów użytkownika](https://medium.com/digital-experience-design/a-guide-to-paper-prototyping-testing-for-web-interfaces-49e542ba765f).

Sprawdzanie założeń w czasie implementacji jest bardzo kosztowne. Przy pomocy papieru - tanie.

## Szmal, kasa, mamona - jak zwał tak zwał.
![EventStorming - co to takiego?!][hotspot]{:.post-left-small-image}
Gdzie jest kasa w tym wszystkim. Przykład projektu który ze względu na nie odpowiednie zaprojektowanie nie został zrealizowany. 
Załóżmy, że projekt mógłby trwać 1 rok i pracowało nad nim 10 osób. 
Zespół w trakcie prac odkrywa, że jest pewnie problem który nie został zauważony bazując tylko na dokumentacji i wymaganiach.
Problem jest na tyle duży, że wymaga przebudowy istotnej części systemu. Daje to dodatkowe 60 dni pracy zespołu.

Do wyliczeń przyjmijmy, że każdy członek zespołu otrzymuje stawkę 100pln/godzinę.

**10 osób * 60 dni * 100pln/godzinę = 480 000 pln.**{:.h-4}

W sesji **Event**{:.event-color}**Storming**{:.command-color}-owej zakładamy 20 uczestników, każda osoba posiadająca wiedzę na temat rozpoznawanego procesu do tego zespół który implementuje rozwiązanie.

Przeprowadzamy dwie sesje po 4 godziny.
W tym czasie zespół modeluje system, konsultuje się między sobą i wykrywa wiele niejasności w stosunku do wymagań i projektu. Konsultacje z klientem, ekspertami i programistami doprowadzają do wyjaśnienia problematycznych obszarów w projekcie.

W trakcie tego procesu istnieje bardzo duża szansa na to, że problem wykryty wyżej w trakcie implementacji został by wykryty. W zasadzie to wykryto by wiele problematycznych miejsc, a dodatkowo stworzony model bardziej odzwierciedlał by to jak faktycznie powinien wyglądać model systemu.
A dlaczego? To proste w procesie modelowania uczestniczyło wiele osób, dyskusje, analizy i rozwikłanie różnych obszarów doprowadziły do lepszego zrozumienia projektu i optymalizacji w miejscach, w których wcześniej nie widzieliśmy. Przecież mamy model na papierze, który łatwo było modyfikować. Bo to papier. 

Bazując na poprzedniej stawce za godzinę.

**20 osób * 8 godzin * 100pln/godzinę =  16 000 pln.**{:.h-4}

Reasumując jeżeli problem został by wykryty na sesji **Event**{:.event-color}**Storming**{:.command-color}-owej to wówczas można mówić o teoretycznym zaoszczędzeniu 464 tyś. pln.
Tak oczywiście to tylko moje wyobrażenia. Jednak mogły by zaistnieć.

Analiza istniejących systemów, tak samo jak i odkrywanie nowych może spowodować odkrycie interesujących miejsc dzięki którym można zoptymalizować aplikację, ulepszyć. Jest całkiem prawdopodobne, że odkrycia i ich eliminacja spowodują oszczędności finansowe.

Myślę, że ten przykład jest przejaskrawiony jednak ukazuje miejsce gdzie skryte są pieniądze.
Stosując **Event**{:.event-color}**Storming**{:.command-color} możemy mieć szansę w ominięciu bagna. 
Skutkiem będzie wykrycie większości problemów jakie napotkali byśmy w trakcie wdrażania już w trakcie sesji **Event**{:.event-color}**Storming**{:.command-color}-owej.

## Na koniec
Ja jestem zafascynowany tym tematem, jeżeli też wzbudziłem w Tobie pożądanie lub przynajmniej chęć użycia swojego otwartego umysłu do zwiększenia świadomości na temat **Event**{:.event-color}**Storming**{:.command-color}-u. To zapraszam na moją listę, będę się dzielił na niej informacjami na temat tej nowej włoskiej techniki przygotowywania pizzy.


**[Ruszyła Szkoła Event Stormingu. Zapraszam.](https://szkolaeventstormingu.pl)**{:.h-1}

[Alberto Brandolini]: https://www.eventstorming.com/
[EventStorming]: {{site.url}}/eventstorming

[post]: /assets/images/2019/02/eventstorming/co-to-takiego/post.png
[post-big]: /assets/images/2019/02/eventstorming/co-to-takiego/post-big.png
[hotspot]: /assets/images/2019/02/eventstorming/co-to-takiego/hotspot.png
[event]: /assets/images/2019/02/eventstorming/co-to-takiego/domain_event.png

[image1]: /assets/images/2019/02/eventstorming/co-to-takiego/image1.jpg
[image1-big]: /assets/images/2019/02/eventstorming/co-to-takiego/image1-big.jpg