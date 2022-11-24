---
title: Jak utrzymywać ADL z wykorzystaniem VSCode?
date: 2022-11-21
author: Krzysztof Owsiany
layout: post
permalink: jak-utrzymywac-adl-z-wykorzystaniem-vscode
published: true
comments: true
image: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/post.jpg
image_big: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/post-big.jpg
categories:
  - Architektura
tags:
  - Architektura
  - ADR
  - ADL
short: Jak dzięki VSCode i adr-tools utrzymywać ADL/ADR w swoim projekcie? Odpowiedź na to pytanie znajdziesz w treści artykułu. Praktyczne porady i polecenia prosto z wymienionych narzędzi. Po przeczytaniu będziesz miał wiedzę, by dokumentować decyzje architektoniczne prosto z VSCode.
---
Jako programista często wykorzystuję różne narzędzia. Tak było tym razem, gdy MS wypuścił swoje nowe LEKKIE narzędzie **Visual Studio Code**. Nie czekałem zbyt długo by skosztować.

I wiesz co? Nie żałuję. **VSCode** wpadło do mojego kanonu narzędzi. I bardzo sobie go cenie.

Zwłaszcza że można bardzo mocno rozszerzać jego możliwości.

Takim ciekawym rozszerzeniem jest **adr-tools**.

O ADRach pisałem więcej w moim poście tutaj -> [Jak używać ADL i ADR w projekcie?]({{site.url}}/jak-uzywac-adl-i-adr-w-projekcie).

To rozszerzenie pozwala na utrzymywanie ADL z wykorzystaniem VSCode.

Trochę automatyzacji nie zaszkodzi…

## Jak przygotować VSCode?

Oczywiście trzeba zainstalować dodatek.

Jest to bardzo proste. Wystarczy użyć ikonki extensions i następnie wyszukać adr-tools.

![Instalacja dodatku adr-tools w VSCode][adr-tools-installation]{:.center-image}
Po instalacji powinieneś mieć dostęp do polecenia adr-tools w **Command Palette**.

![Command Palette po instalacji adr-tools][command-palette]{:.center-image}

## Utworzenie ADL z wykorzystaniem adr-tools.
Pierwsze użycie będzie wiązało się z użyciem polecenia ADR Init.

Po wyborze otrzymasz pytanie gdzie składować Twoja dokumentację?

![Ustawianie katalogu dla ADLa][set-folder]{:.center-image}

Ustawiasz wedle uznania. Ja wybrałem katalog doc\adl

Następnie trzeba wskazać domyślną templatkę dla wpisów ADR.

![Ustawianie templatki dla ADRów][set-template]{:.center-image}

Ja użyję tej sugerowanej. Twój wybór może być oczywiście inny. Możesz przygotować własną templatke zgodnie z własnymi upodobaniami.

Ostatni krok to wskazanie katalogu, w którym znajdzie się templatka. Ja tutaj też zatwierdzam enterem i przechodzę dalej.

To był ostatni krok i moim oczom ukazały się dwa katalogi jak na zrzucie.

![Po utworzeniu ADLa][after-init-adl]{:.center-image}

Jest templatka i poniżej pierwszy wpis z numerem 0000…

## Tworzenie ADRów.

Dodawanie kolejnego wpisu to już użycie ADR New.

![Dodawanie nowego ADRa][new-adr-1]{:.center-image}

Po wyborze polecenia dodawania ADRa.

Należy wprowadzić jego nazwę, jaka będzie znajdować się po kolejnym numerze identyfikacyjnym.

![Ustawianie nazwy nowego ADRa][new-adr-2]{:.center-image}

Następnie określić status.

![Ustawienie statusu ADRa][new-adr-3]{:.center-image}

Możemy wskazać relację do jakiegoś innego wpisu. Ja tutaj wybieram None.

![Ustawienie relacji z innym ADRem][new-adr-4]{:.center-image}

Natomiast jeżeli wybierzesz inną opcję. To będziesz musiał wskazać powiązanego ADRa.

I tak oto dodałem kolejny wpis. 

![Nowy wpis dodany][new-adr-5]{:.center-image}

## Pozostałe polecenia

Oczywiście pozostałe polecenia także są pomocne. Możesz na przykład powiązać istniejące ADRy przy pomocy polecenia ADR Link. Wskazujesz wówczas: ADR źródłowy, relację i ADR docelowy.

Możliwa jest też zmiana statusu przy pomocy ADR Status. Wówczas wskazujesz ADRa do zmiany i ustawiasz status, jaki chcesz.

Możesz też wygenerować dokumentację z wykorzystaniem Adr Generate documentations. To jednak już pozostawiam Twoim własnym eksperymentom.

## O konfiguracji
Konfiguracja, jaką ustawiłeś podczas użycia ADR Init. Znajduje się w .vscode/settings.json.

![Konfigurowanie adr-tools][configuration]{:.center-image}

Możesz ją zmienić jeżeli, jest taka potrzeba.

PS: Co sądzisz o ADLach w VSCode i samym narzędziu adr-tools?

PS: Więcej o ADL i ADR znajdziesz w moim poście: [Jak używać ADL i ADR w projekcie?]({{site.url}}/jak-uzywac-adl-i-adr-w-projekcie)

PS: Zainteresował cię temat? Zajrzyj do mojego newslettera: [Model C4](https://modelc4.pl).

---
[post]: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/post.jpg
[post-big]:/assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/post-big.jpg


[adr-tools-installation]: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/adr-tools-installation.png
[after-init-adl]: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/after-init-adl.png
[configuration]: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/configuration.png
[new-adr-1]: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/new-adr-1.png
[new-adr-2]: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/new-adr-2.png
[new-adr-3]: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/new-adr-3.png
[new-adr-4]: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/new-adr-4.png
[new-adr-5]: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/new-adr-5.png
[command-palette]: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/command-palette.png
[set-folder]: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/set-folder.png
[set-template]: /assets/images/2022/11/jak-utrzymywac-adl-z-wykorzystaniem-vscode/set-template.png
