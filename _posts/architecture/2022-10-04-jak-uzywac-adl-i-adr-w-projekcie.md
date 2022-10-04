---
title: Jak używać ADL i ADR w projekcie?
date: 2022-10-04
author: Krzysztof Owsiany
layout: post
permalink: jak-uzywac-adl-i-adr-w-projekcie
published: true
comments: true
image: /assets/images/2022/10/jak-uzywac-adl-i-adr-w-projekcie/post.jpg
image_big: /assets/images/2022/10/jak-uzywac-adl-i-adr-w-projekcie/post-big.jpg
categories:
  - Architektura
tags:
  - Architektura
  - ADR
  - ADL
short: Architektura systemów IT często ulega zmianie. Wynika to z różnych przyczyn. Jednak najczęściej (w moim przypadku) zmiana była wynikiem próby nadążenia za zmieniającym się biznesem. Dla biznesu to nie jest wielki problem. Ot, tak dodaj tu buttona.
---
Architektura systemów IT często ulega zmianie. Wynika to z różnych przyczyn. Jednak najczęściej (w moim przypadku) zmiana była wynikiem próby nadążenia za zmieniającym się biznesem. Dla biznesu to nie jest wielki problem. Ot, tak dodaj tu buttona. Tam checkboxa a najlepiej to jak byś przyśpieszył generowanie raportów, bo teraz to jest bardzo czasochłonne i klienci się niecierpliwią.

Zapewne słyszałeś takie lub podobne pomysły. Niczym jeden krzyk wywołujący lawinę śniegu. Biznes prędzej czy później się zmieni w pogoni za światem. Także będzie ulegała zmianie architektura systemów. Będzie ewoluować.

Utrzymanie systemów informatycznych to duża odpowiedzialność. Wiedzę dotycząca ich budowy jest tutaj kluczowa. Dlatego dobrze by było wiedzieć, dlaczego akurat w tym module używamy CosmosDB a w innym PostgreSql?

Po miesiącach czy latach rozwoju softu możemy zapomnieć, jakie były powody wyboru tych technologii.

Może też nastąpić rotacja pracowników i możemy pozostawić następcy mały prezent w postaci historii zmian architektury.

I najlepiej kto pozwolił na wykorzystanie tych technologii? → Kto to tak spier….

Dobrym miejscem przechowania takich informacji są system kontroli wersji. To nie tylko miejsce przechowywania kodu źródłowego. To też przestrzeń dla dokumentacji. Także architektury całego systemu. Blisko kodu, pod ręką.


## Jak to robić?
Zapewne już ktoś to wymyślił? Tak to prawda. Istnieją do tego metody.

Jednak na początek trochę teorii.

Mianem historii zmian architektonicznych określamy **ADL**, czyli **Architecture Decision Log**.

Log zawierający wszelkie istotne z punktu widzenia architektury wpisy (zmiany).

Początkowy wybór technologii to także pewna decyzja do zanotowania.

Każdy taki pojedynczy wpis jest określany jako **ADR**, czyli **Architecture Decision Record**.

Tym samym ADL ma rolę organizacyjną i można określać jego mianem np. arkusz Excela zawierający wpisy ADR.

Jednak kto by chciał to robić w Excelu... Mamy przecież GITa….

Najlepiej to jeszcze by łatwo to było formatowane i proste w edycji.

Tym sposobem wchodzimy w świat Markdowna.


## Wzór ADRu.
W internecie można spotkać wiele wzorów decyzji architektonicznych.

Tutaj jest jeden ze zbiorów: [https://github.com/joelparkerhenderson/architecture-decision-record](https://github.com/joelparkerhenderson/architecture-decision-record)

Przykładowy ADL znajdziesz tutaj: [https://docs.devland.is/technical-overview/adr](https://docs.devland.is/technical-overview/adr)

Bardziej lub mniej skomplikowane. Wybór należy do zespołu. Ludzi, którzy podejmują pierwsze decyzje co do wyglądu architektury i samego ADRa.

Polecam na początek użyć prostego wzorca zaproponowanego przez Michaela Nygard. Przedstawia go w swoim wpisie: [https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)

Taki wpis zawiera w sobie serie nagłówków i opis.


**Title**

Taka decyzja powinna mieć tytuł. Dla łatwej identyfikacji przeznaczenia wpisu.


**Context**

Kontekst to opis zawierający informację na temat powodów zmiany architektury.

Dlaczego taka zmiana była konieczna?

Jakie motywy kierowały ówczesnym zespołem.


**Decision**

Opis podjętej decyzji. Czyli co zamierzamy zmienić. Jak chcemy rozwiązać zaistniały problem.


**Status**

Taki wpis może mieć swój status. Warto by było to też gdzieś opisane.

Decyzja może być np. zaakceptowana, odrzucona, cofnięta, zaproponowana.


**Consequences**

Konsekwencje wprowadzonej decyzji. Jakie będą skutki dla systemu po wprowadzonych zmianach.



## Jak nazywać pliki z ADRami?

Dorze, by było mieć też pewien dokument zawierający opis używanego wzorca ADRu. Tak by każdy, kto wprowadza takie wpisy. Wiedział, jak używać. Jakie statusy ma do dyspozycji. Tym samym nie wymyślać nowych a jak takowe wejdą do użycia zaktualizować dokument.

To może być prosty dokument readme.txt znajdujący się wewnątrz ADLa.

Takie wpisy bez jednego ważnego elementu będą chaotyczne i prawie bezwartościowe.

Jest nim oczywiście odpowiednie oznaczanie wpisów. Wedle ich wprowadzania np. sekwencją 0001, 0002, 0003….000n. Można też w nazwie pliku, wskazać czego dotyczy ADR.

np. **0003_use_cqrs.md**

Numeracja wprowadzi hierarchię do loga. Przedstawi prawdziwy bieg wydarzeń.

Jeżeli przykładowy wzorzec nie jest dla Ciebie satysfakcjonujący. To dodaj, co potrzebujesz:

Autora zmiany, datę zmiany, odniesienia do diagramów architektonicznych np. [Modelu C4]({{site.url}}/10-powodow-dla-ktorych-warto-znac-model-c4).

PS: Warto, także w repozytorium utrzymywać diagramy zgodnie z ADLem. Czyli tak zwane **Diagram as Code**. Czy to będzie kod C#, Java, PlantUML to już twoja decyzja. Jednak ważne by ADL szedł zgodnie z diagramami.

Zainteresował cię temat? Zajrzyj do mojego newslettera: [Model C4](https://modelc4.pl).

---
[post]: /assets/images/2022/10/jak-uzywac-adl-i-adr-w-projekcie/post.jpg
[post-big]:/assets/images/2022/10/jak-uzywac-adl-i-adr-w-projekcie/post-big.jpg
