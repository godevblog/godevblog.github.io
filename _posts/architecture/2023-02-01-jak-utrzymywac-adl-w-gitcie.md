---
title: Jak utrzymywać ADL w GITcie?
date: 2023-02-01
author: Krzysztof Owsiany
layout: post
permalink: jak-utrzymywac-adl-w-gitcie
published: true
comments: true
image: /assets/images/2023/02/jak-utrzymywac-adl-w-gitcie/post.jpg
image_big: /assets/images/2023/02/jak-utrzymywac-adl-w-gitcie/post-big.jpg
categories:
  - Architektura
tags:
  - Architektura
  - ADR
  - ADL
  - GIT
  - Conventional Commits
short: Używam komputerów od wielu lat. Jestem dinozaurem, zaczynałem w latach 90. Dla wielu osób to już nie senior developer tylko grandfather developer. W poście odnoszę sie do związku jaki ma PC bałagan i ADL.
---
Używam komputerów od wielu lat. Jestem dinozaurem, zaczynałem w latach 90.

Dla wielu osób to już nie senior developer tylko grandfather developer.

Pomijając etykiety prędzej czy później na tym PC zawsze robił się błaga.

Sprostuję. Ja robiłem bałagan. Najprościej było wrzucić stary dysk do katalogu w nowym i po problemie.

Do dzisiaj mam takie zasoby…

Teraz wyobraź sobie bajzel w dokumentacji architektury… Nie możesz do tego dopuścić.

Dlatego pomimo wymienienia kilku sposobów na utrzymanie ADLa w moim poście [tutaj]({{site.url}}/jak-uzywac-adl-i-adr-w-projekcie).

Najlepiej jak użyjesz systemu kontroli wersji i automatyzacji, jaką daje np. adr-tools → [więcej o narzędziu tutaj]({{site.url}}/jak-utrzymywac-adl-z-wykorzystaniem-vscode).


## GIT
Dla mnie nie ma innego wyboru. Odkąd nauczyłem się używać w konsoli + VIM xD. To unikam innych narzędzi. Polecam i Tobie konsole GITa. Działa w niej wiele poleceń z linuxa. Jeżeli masz Windowsa, to może być dodatkowy atut ;).

No tu już pewnie się domyślasz, że polecam repo GITa jako narzędzie do utrzymania ADLa.

Jako że przeważnie mamy więcej możliwości w danej chwili. To pomimo wyboru systemu kontroli wersji nadal otwierają się dylematy.

A to osobne repo dla dokumentacji i kodu?

A może wszystko razem?

Odpowiedź jak dla mnie — to zależy — od Ciebie i teamu.

Dla mnie naturalnym wyborem jest utrzymanie dokumentacji architektury przy projekcie. W tym samym repozytorium.

## Konwencja.
Zanim jednak przejdę do konkretów. Może trochę o konwencji, jaką możesz przyjąć.

To ponownie tylko moja sugestia, ale zainteresuj się Conventional Commits. Jest to pewna konwencja pisania commit message. 
Taki commit, ma pewne oznaczenie. Sugeruje ono, co tam się znajduje. Czy to jest fix, feature, refactor, test itd.
Jeżeli się tego będziesz trzymał. To będzie to też pomocne przy ograniczeniu rodzaju zmian w jednym commicie.
By nie pchać wszystkiego na raz tylko testy osobno, kodzik osobno itd.

Ja proponuje wzbogacenie CC o nowe oznaczenia:
* devops — wiadomo jakieś pipeliny, templatki itd.
* adl lub adr - opis architektury
* arch — zmiana architektury np. aktualizacja modelu C4 → [więcej o C4]({{site.url}}/10-powodow-dla-ktorych-warto-znac-model-c4).

Takie oznaczenia ciekawie wyglądają podczas wyświetlenia listy commitów.

O tak…
![Polecenie wyświetlenia logów][git-log]{:.center-image}
Po instalacji powinieneś mieć dostęp do polecenia adr-tools w **Command Palette**.

I tak…
![Wygląd logów GITa z Conventional Commits][gitlogs]{:.center-image}

## Przykładzik.
Teraz pozostaje już tylko utworzyć folder (doc/adl) na dokumentację architektury i utrzymywać tam ADRki.

Możesz skorzystać z templatki i VSCode. Nawet jak używasz innego narzędzia, które nie wspiera templatek ADL. To możesz dla samej architektury użyć VSCode do ich utrzymania.

![Katalog doc zawierający ADL][doc-adl]{:.center-image}

Więcej o templatkach w moim poprzednim wpisie.

Same polecenia GITa to już banały:

* git add -p /doc/adl - dodanie nowych ADRów wraz z przeglądem zmian (parametr -p)
* potwierdzanie zmian (dla polecenia wyżej) odpowiednio y - yes, n - no
* git commit -m"adr: add new adr entry for CQRS"
* na koniec git push…


I tak oto łączysz GITa, Conventional Commits i ADL.

Jeszcze tylko Diagram as Code i wszystko jest w jednym miejscu.

PS: Co sądzisz o używaniu GITa do utrzymywania logów decyzji architektonicznych?

PS: Więcej o ADL i ADR znajdziesz w moim poście: [Jak używać ADL i ADR w projekcie?]({{site.url}}/jak-uzywac-adl-i-adr-w-projekcie)

PS: Zainteresował cię temat? Zajrzyj do mojego newslettera: [Model C4](https://modelc4.pl).

PS: Jak używać VSCode do tworzenia ADRów? Dowiesz się z mojego posta -> [Jak utrzymywać ADL z wykorzystaniem VSCode?]({{site.url}}/jak-utrzymywac-adl-z-wykorzystaniem-vscode)

---
[post]: /assets/images/2023/02/jak-utrzymywac-adl-w-gitcie/post.jpg
[post-big]:/assets/images/2023/02/jak-utrzymywac-adl-w-gitcie/post-big.jpg
[git-log]: /assets/images/2023/02/jak-utrzymywac-adl-w-gitcie/git_log.png
[gitlogs]: /assets/images/2023/02/jak-utrzymywac-adl-w-gitcie/gitlogs.png
[doc-adl]: /assets/images/2023/02/jak-utrzymywac-adl-w-gitcie/doc_adl.png