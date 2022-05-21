---
title: 10 powodów, dla których warto znać Model C4.
date: 2020-12-22
author: Krzysztof Owsiany
layout: post
permalink: 10-powodow-dla-ktorych-warto-znac-model-c4
published: true
comments: true
image: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/post.png
image_big: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/post-big.png
categories:
  - Model C4
tags:
  - Architektura
  - Model C4
  - C4
short: Czy znasz Model C4? A może nie wiesz, dlaczego warto zapoznać się z tym Terminem? W artykule przedstawiam 10 powodów. Dlaczego jest to temat gody uwagi. Przeczytaj poniższy tekst, a zainteresujesz się tematem.
---
Chcesz wiedzieć, dlaczego **Model C4** jest Ci potrzebny? Myślę, że jesteś w dobrym miejscu.

Pracowałem kiedyś w pewnej firmie nad dużym projektem. Oczywiście nie mogę zdradzić konkretów.
System miał obsługiwać sporą bazę pracowników oraz klientów w całej Polsce.

Pomyślisz sobie. Pewnie był skomplikowany. I słusznie był...
W takiej sytuacji dobrze by było posiadać skondensowaną wiedzę w postaci narysowanego diagramu. Komponentów systemu było wiele.

[![Odręcznie rysowana warstwa modelu Model C4.][c4draw]{:.post-center-image}][c4draw-big]

Jak się okazało, taki model architektury istniał. Jednak to, w jaki sposób został sporządzony i jakie informacje zawierał - pozostawiało wiele do życzenia. Powiem inaczej. Więcej to wprowadzało niezrozumienia, zamieszania niż wartości.
Diagram był narysowany jak przez dziecko w przedszkolu. Zapewne o średnich zdolnościach artystycznych.
Kompletnie go nie rozumiałem. Chaotyczne linie łączące różno-kształtne elementy. Skróty, które w zasadzie nic nie mówiły.
Tylko usiąść i płakać. Jednak jako bohater tej historii. Tego nie uczyniłem. Kilka miesięcy potem zmieniłem pracę :). Diagram nie był głównym powodem.

Jeżeli podobna sytuacja nie jest Ci obca. To już masz jeden powód, by skierować swoje zainteresowanie do **Modelu C4**.

Dam Ci ich znacznie więcej. Tylko czytaj dalej.

## 1. Podział na 4 warstwy.

**Model C4** opiera się o rozdzielenie opisu architektury na cztery warstwy abstrakcji.
Każda z nich odgrywa inną rolę. Posiada zróżnicowane cechy i odmienne zawiera odmienne szczegóły.
Dzięki temu może być kierowana do programistów, architektów, PO itd. Czyli osób o odmiennych rolach w zespole czy firmie.

Wyróżniamy. Jak nazwa wskazuje 4 warstwy:
* **C1 - Context System**
* **C2 - Containers**
* **C3 - Components**
* **C4 - Code**.

W pewnym sensie można zauważyć tutaj podejście od ogółu do szczegółu.

## 2. Rozproszenie informacji na różne diagramy architektoniczne.

Jak pisałem wyżej. Spotkałem na swojej drodze diagramy opisu architektury. Przeważnie były to coś, co przypominało bigos lub spaghetti. Wszystkie informacje wymieszane razem. Elementy systemu na jednym rysunku połączone strzałkami. Brak podkreślenia znaczenia lub przeznaczenia konkretnych bloków na diagramie. Krzywo rysowane (koślawe) elementy.

[![ModelC4 - warstwa C2 - kontenery.][modelc4-c2]{:.post-center-image}](https://modelc4.pl)

Model C4 wprowadza organizację do wizualizacji architektury. Poszczególne warstwy wymienione w pkt. 1 Nie tylko dzielą system. Stanowią także zlepek odrębnych informacji. Razem to całość schowana pod płaszczykami warstw. Osobno to wystarczający opis fragmentu z całego systemu. Mniej szczegółów oznacza mniej trudności ze zrozumieniem.

## 3. Możliwość programowania wizualizacji architektury w wielu językach.

Do tworzenia wizualizacji w modelu C4. Możesz wykorzystać jeden z popularnych języków programowania.
Oczywiście **C#** jest jednym z nich. Kilka innych, z jakich możesz skorzystać to: **JAVA**, **TypeScript**, **PHP**, **GO**, **Python**, **DSL**, **YAML**. Jest tego sporo. I jak się okazuje nie wszystkie to jednak języki.

[![ModelC4 - warstwa C4 - kod.][modelc4-c4]{:.post-center-image}](https://modelc4.pl)

Dzięki wykorzystaniu programowania nie trzeba używać GUI. Zapewne wiele osób będzie zadowolona z takiego stanu rzeczy. Dzięki wykorzystaniu narzędzia **[Structurizer](https://structurizr.com/)**. Możesz wygenerować wizualizację na bazie kodziku lub np. YAMLa.

Jak dla mnie całkiem przydatna sprawa. Także za sprawą kolejnych pkt. z listy. Czytaj dalej.

## 4. Historia zmian w systemie kontroli wersji.

Skoro można programować. To grzechem byłoby nie korzystać z narzędzi kontroli wersji.

Będzie to najlepsza historia rozwoju systemu architektury systemu. 

Zapewne znasz architekturę ewolucyjną? Jeżeli nie to zapraszam do mojej [biblioteczki](https://mrdev.pl/biblioteczka#Architektura). Znajduje się tam w kategorii architektura książka na ten temat.

Chodzi przede wszystkim o to, że tak jak biznes oraz kod zmianie ulega architektura. W trakcie rozwoju zapewnić musimy odmienne drivery architektoniczne. System zmienia się i stawia przed nami odmienne wymagania.
Dzięki wykorzystaniu programowania do opisu architektury.

Utrzymywaniu tego wszystkiego w repozytorium takim jak **GIT**. Możemy śmiało dokonywać poprawek. Poddawać potem to pod **CodeReview**. I rozwijać wraz z projektem.

Można wpleść to do swojego flow agileowego lub innego. Jako stały element.


## 5. Wykorzystanie ADL i ADR

Wygląda na to, że punkty się ze sobą łączą. Nie planowałem tego, samo wyszło. 

Programowanie architektury w modelu C4 można połączyć z **ADL (Architecture Decision Log)** oraz **ADR (Architecture Decision Record)**.

Wówczas to właśnie w **ADLu** możesz umieszczać kodzik odpowiedzialny za wizualizację architektury.
Następnie wraz z nanoszeniem istotnych zmian w modelu. Dokonywać odpowiednich wpisów z wykorzystaniem **ADRów**.
To propozycja na zbudowanie **ADL** z wykorzystaniem repozytorium. Myślę, że jest to ciekawe podejście.

**Czy już zainteresowałem cię tematem? Chcesz więcej? Zapraszam na mój newsletter [ModelC4.pl](https://modelc4.pl).**{:.h-4}

[![ModelC4.pl - newsletter][modelc4]{:.post-center-image}](https://modelc4.pl)

**Po zapisie i potwierdzeniu. Dostaniesz serię e-maili dotyczących C4. Będę tam też zamieszczał najlepsze oferty dołączenia do klanu [Modelu C4](https://modelc4.pl).**{:.h-4}


## 6. Prosty w zrozumieniu.

Mniej szczegółów w jednym miejscu to większa przejrzystość. To często wpływa na czytelność i zrozumienie. Podział na warstwy pełniące różne role pozwala na selekcję informacji. Jeżeli trafimy do osoby nietechnicznej z odpowiednią warstwą. To zapewne zrozumie więcej. Niż jak by dostała cały diagram naszkicowany na kartce A1.

Zapewne przesadzam. Jednak często nie zdajemy sobie sprawy. Jak nie zrozumiałe są nasze opisy. I bez głębszego posiedzenia i analizy odbiorca może nie zrozumieć.

Może też błędnie zrozumieć. Niezrozumienie siebie nawzajem to bardzo duży problem w IT. Zwłaszcza na linii programiści — biznes.

[![ModelC4 - warstwa C1 - kontekst systemu.][modelc4-c1]{:.post-center-image}](https://modelc4.pl)

Widziałem to często podczas prowadzenia warsztatów z **[EventStormingu]({{site.url}}/eventstorming-co-to-takiego)** jak z czasem złoto skryte w rudzie. Szlifowane, obrabiane ukazywało swoje piękno coraz to większej grupie uczestników. Z czasem dochodziło do zrozumienia, złożonych problemów. 

Czy tak samo musi być z architekturą? Czy nie lepiej opierać się o proste elementy i stosować wyklarowany mechanizm i podstawowe komponenty?

Mam wrażenie, że prostota jest istota. I powinna być także dla Ciebie. Model C4 pozwala uprościć nasze wymysły, jakie tworzymy w trakcie projektowania architektur systemów.


## 7. Czytelna wersja elektroniczna.

Lubię rysować. Bloczki, walce. Łączyć je w całość. Niech stanowią odwzorowanie części rzeczywistości.
Niestety pismo mam tragiczne. Staram się, ale w trakcie, gdy chwytam flow. Forma przesłaniana jest treścią XD.

Niestety jest to bardzo nieczytelne. Nawet dla mnie. Wręcz łapię się na tym, że czasem nie rozumiem, co napisałem. Całe szczęście jest jeszcze komputer i można po normalnemu coś napisać...

I jak tu rozrysować czytelny schemat architektoniczny...

[![ModelC4 - warstwa C3 - komponenty.][modelc4-c3]{:.post-center-image}](https://modelc4.pl)

Ano tak. Przecież jest Model C4. Pozwala zrzucić ze mnie i Ciebie ten balast. Nie trzeba się już tak bardzo przejmować rysowaniem. Zrobić to może za nas **[Structurizer](https://structurizr.com/)**. 

Oczywiście trzeba nauczyć się użytkowania. Także nie jest to całkowicie darmowe narzędzie (jeden diagramik możesz utrzymywać za free). 

Natomiast robi robotę. Dostarcza ładny diagram. Wystarczy odpowiednio oprogramować elementy.

**Czytelność w mojej opinii nieporównywalna.**

## 8. Relacje pomiędzy elementami.

Tak jak wyżej wspominałem. Model C4 podzielony jest na cztery warstwy. Każda z niższych warstw, rozszerza pewien fragment wyższej. Takie przybliżenie lupą. 

Do tego, jeżeli jest to z wizualizowane za pomocą **Structurizera**. Masz możliwość nawigowania. Klikasz w bloczek i rozwija ci się niższa warstwa. Powiązane ze sobą elementy na różnych warstwach pozwalają na rozwijanie szczegółów.

Dlatego jest to takie czytelne. Nie widzimy od razu całej złożoności tylko pewien wycinek rzeczywistości. 

[![ModelC4 - relacje między warstwami.][modelc4-relacje]{:.post-center-image}](https://modelc4.pl)


Ze szczegółami systemu, zapoznajesz się poprzez zagłębianie krok po koku w elementy i warstwy architektury modelu.

Można go porównać do drzewa. Zaczynając od pnia. Przechodzimy w górę do grubszych odnóg, gałęzi i liści.

Z tą różnicą, że w C4 nie podziwiamy całego drzewa od razu. Tylko ukrywane są przed nami poszczególne jego fragmenty.


## 9.  Możliwość dostosowania do siebie.

Model C4 lansuje pewien wzorzec. Konkretne elementy, jakie można wykorzystywać na poszczególnych warstwach. Do tego pewne kolory. 

Oczywiście możesz to wszystko adoptować do siebie, zespołu czy firmy. Jednak stosowanie pewnej wypracowanej formy niesie ze sobą także wartość. Jest szansa, że ktoś po drugiej stronie. Zrozumie w lot, gdyż zna C4 i podstawowe elementy.
   

## 10. Możliwe użycie w procesie Continuous Integration.

Ciągła integracja to obecnie często mus w projektach. Niesie ze sobą wirtualnego niewolnika. Pracującego w pocie czoła nad projektem.

Możesz w cały proces wpleść budowanie wizualizacji. Jeżeli masz opis architektury w kodziku i repozytorium.
Wystarczy wrzucić w cykl budowania aplikacji. Oczywiście dowolnie wedle własnego uznania.
Generować nową wizualizację. Jak się coś zmieni w repo. To niech zajmie się tym **DevOps**, **Jenkins**, **TeamCity**, **Travis** czy inne narzędzie. A ty ciesz się z automatyzacji.


I tak dotarłeś do końca. Jeżeli masz jakieś wątpliwości, pytania to postaram się na nie odpowiedzieć.
Wystarczy, że napiszesz komentarz, do czego zachęcam Lub bardziej intymnie, czyli na mojego e-maila: [krzysztof@mrdev.pl](mailto:krzysztof@mrdev.pl).

**Zachęcam także do zapisania się na [https://modelc4.pl](moją listę mailową). E-maile na temat Modelu C4 czekają na Ciebie.**{:.h-2}

[![ModelC4.pl - newsletter][modelc4.pl-logo]{:.post-center-image}](https://modelc4.pl)

---
[post]: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/post.png
[post-big]: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/post-big.png

[modelc4]: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/c4.gif
[modelc4.pl-logo]: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/model_c4_181x64.png
[modelc4-relacje]: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/c4_model.jpg
[modelc4-c1]: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/c1_context.jpg
[modelc4-c2]: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/c2_containers.jpg
[modelc4-c3]: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/c3_components.jpg
[modelc4-c4]: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/c4_code.jpg

[c4draw]: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/c4draw.jpg
[c4draw-big]: /assets/images/2020/12/10-powodow-dla-ktorych-warto-znac-model-c4/c4draw-big.jpg