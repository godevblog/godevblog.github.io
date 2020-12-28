---
title: Continuous Integration, Delivery, Deployment.
date: 2019-01-22
author: Krzysztof Owsiany
layout: post
tags:
  - CI
  - CD
  - Continuous Delivery
  - Continuous Integration
  - Continuous Deployment
comments: true
permalink: continuous-integration-delivery-deployment
published: true
image: /assets/images/2019/01/continuos-integration-delivery-deployment/post.jpg
image_big: /assets/images/2019/01/continuos-integration-delivery-deployment/post-big.jpg
categories:
  - CI
  - CD
short: Dzisiaj zabiorę Cię w daleką podróż do świata automatyzacji. Gdzie build-y same się wykonują. A o dowiezieniu do komputera decyduje automat lub czasem jakaś gruba ryba w firmie. Tak mowa oczywiście o Continuous Integration + Continuous Delivery/Deployment.
---
![Continuous Integration, Delivery, Deployment!][post-big]

Bardzo dawno temu gdy człowiek chciał wyjechać do chAmeryki. Musiał najpierw zebrać trochę grosza by mieć na podróż. A potem różnymi środkami przedostać się z miejsca początku swojej podróży na statek. Korzystał z różnych sposobów lokomocji, piechota, muły, pociągi. Ostatecznie gdy znalazł się już w porcie to albo legalnie albo na dorobku podróżował do chAmeryki. Podróż jak widać byłą bardzo trudna, nie zawsze się udawało. Było to bardzo ryzykowne, można było stracić zdrowie ale także życie.

X czasu później. Jedziemy własnym samochodem/taksówką lub zamawiamy Uber-a. Prosto na lotnisko, wcześniej mamy już miejsce zarezerwowane. I w kilkanaście godzin jesteśmy w chAmeryce. Dawniej to trwało tygodnie...

Aluzja jest tutaj oczywista. Jeszcze nie tak dawno lub nawet niektórzy nadal dostarczają oprogramowanie w formie spakowanych zipów. Po drodze przechodząc przez różne problemy.
Proces ten jest bardzo podatny na błędy. Wystarczy nie uwzględnić zmiany jednego malutkiego pliku, a deploy będzie nie pełny.

[![Continuous Delivery][image1]][image1-big]{:.post-left-image}

Jak by ktoś nie wiedział programiści to leniwe stworzenia. Jak tylko mogą to będą dążyli do błogiego statu nie robienia nic. Tworzą różnego rodzaju narzędzia i skrypty by tylko całą robotę zwalić na biedne komputery.

Nie inaczej jest też w tym przypadku, leniwce opracowały pewne mechanizmy automatyzujące proces dostarczania oprogramowani od programisty do konsumenta.
Między tymi dwiema osobami stoi zautomatyzowany proces. A przynajmniej powinien stać taki proces ;)

By nie było lekko i czasem zabawnie. Występują tutaj dwie grupy o skrócie **CD**. Z drugiej strony może taki był zamysł stwórcy. 

**Continuous Deployment i Continuous Delivery występują zamiennie.**{:.h-1}

Został on podzielony na kilka mniejszych grup działań:

* **CI - Continuous Integration**{:.color_2} - jest pierwszym etapem w dowiezieniu oprogramowania do klienta, odpowiada za konsumpcje zatwierdzeń w kodzie wykonanych przez sprytnych programistów np. korzystających GIT-a. I na tej podstawie zweryfikowanie czy testy się poprawnie wykonują, czy następnie aplikacja buduje się. Daje feedback koderowi jeżeli pójdzie coś nie tak ;). Dopiero prawidłowe przejście tego procederu pozwala na dalsze kroki jakie wykonuje grupa **CD**. Sprawdza i daje zielone lub czerwone światło. Od tego zależy los zmian dokonanych przez programistę.
  
* **CD - Continuous Deployment**{:.color_2} - kontynuujemy zatem dowożenie oprogramowania do klienta, po prawidłowym przejściu **CI** możemy wydawać paczuszki do dalszych testów lub od razu do klienta na produkcję (to już zależy od wewnętrznej polityki  zespole/firmie). Ten proces ostatecznie zamieszcza wprowadzone zmiany w docelowym miejscu gdzie się mają znaleźć. 
  
* **CD - Continuous Delivery**{:.color_2} - w zasadzie nie ma co tutaj pisać za dużo. Funkcjonuje prawie tak samo jak Continuous Deployment. Jednak tutaj mamy czynnik ludzki w każdym dowiezieniu gotowego produktu do klienta lub na środowiska testowe. Trzeba zatwierdzić czy chce się dokonać aktualizacji. Musi być jakiś pan Kowalski lub kilku Kowalskich, posiadających tajemną moc sprawczą nad aktualizacją oprogramowania.

[![Continuous Deployment][image2]][image2-big]{:.post-right-image}

Można tutaj rozwinąć z języka angielskiego by było łatwiej:
* **Continuous**{:.color_2} - oznacza coś ciągłego, trwającego.
* **Deployment**{:.color_2} - to ulokowanie czegoś, zamieszczenie tym samym mam to co chcemy w miejscu docelowym. 
* **Delivery**{:.color_2} - dostarczamy gotowe rozwiązanie ale tylko dostarczamy. Tak jak kurier dostarcza paczkę ale nie musimy odbierać:) lub rozpakowywać

Już słyszę głosy iście z PRL-u. Za moich czasów to robiło się inaczej. Z dwóch ludzi miało pracę...
Tak ale ile to trwało?
Sam jestem namacalnym dowodem na to że taka ewolucja działa. Gdy tylko natknąłem się na tą tematykę rzuciłem się niczym wygłodniała hiena na mięso.
Wdrożyłem po wielu trudnych i znojach. 
- I co się zmieniło?
- A nic panie, wcześniej to każdy pliczek musiałem ręcznie na FTP-a wrzucać, a ile było w tym pomyłek gdy nie wrzuciło się jakieś graficzki....
- Teraz to ja kasuje linie kodu, zatwierdzam wpycham i dzieje się samo. Po 5 minutach można wykonać aktualizację.

Wiem, że nadal ten proces funkcjonuje ile sobie i innym stresu zaoszczędziłem wdrażając takie rozwiązanie...

**Jeżeli jeszcze nie używasz to zacznij! Jest w tym moc!**{:.h-2}



[post]: /assets/images/2019/01/continuos-integration-delivery-deployment/post.jpg
[post-big]: /assets/images/2019/01/continuos-integration-delivery-deployment/post-big.jpg

[image1]: /assets/images/2019/01/continuos-integration-delivery-deployment/image1.jpg
[image1-big]: /assets/images/2019/01/continuos-integration-delivery-deployment/image1-big.jpg

[image2]: /assets/images/2019/01/continuos-integration-delivery-deployment/image2.jpg
[image2-big]: /assets/images/2019/01/continuos-integration-delivery-deployment/image2-big.jpg