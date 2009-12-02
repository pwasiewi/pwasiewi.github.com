---
layout: default
title: Liniowa regresja - zmiany w skryptach
---

Zmieni³a siê struktura skryptów z [GitHub-u](http://github.com/pwasiewi) uzyskiwanych komend±:

`git clone git://github.com/pwasiewi/iso.git`

Tworzy ta komenda katalog iso, a w nim nowe skrypty umieszcza. Plik *isowitdatasets.r* jest tym razem headerem zawieraj±cym definicje zbiorów danych i ich domy¶lne przetwarzanie np. dyskretyzacja, zescorowanie i specyficzne zbiory nazw atrybutów do dalszego stosowania. Po zmodyfikowaniu na pocz±tku ka¿dego z plików: *isowitoptimlm.r*, *isowitalterlm.r*, *isowitoptimklas.r*, *isowitreglog.r* ¶cie¿ki do skryptu z koñcówk± "..../iso" zwanej dalej <¶cie¿ka do pliku>, uruchamiamy R i wpisujemy:

`source("<¶cie¿ka do pliku>/isowitoptimlm.r")` 

* Skrypt przetwarzaj±c permutacje zmiennych obja¶niaj±cych (dla n od 1 do liczby wszystkich atrybutów wej¶ciowych) wybiera najlepsz± regresjê liniow± wed³ug parametru r-square R2 dopuszczaj±c regresje z wariancj± równomiernie roz³o¿on± st±d testy levena i bptest na heterowariancjê

`source("<¶cie¿ka do pliku>/isowitalterlm.r")`

* Skrypt porównuje alternatywne formy uzyskiwania najlepszej regresji z redukcj± atrybutów lub i bez niej na podstawie kryteriów AIC i BIC oraz Ridge

`source("<¶cie¿ka do pliku>/isowitoptimklas.r")`

* Skrypt znajduje stosuj±c permutacje atrybutów o d³ugo¶ci od 1 do liczby wszystkich atrybutów wej¶ciowych najlepszy klasyfikator dla metod rpart, J48, svm, ipredknn, lda, NaiveBayes

`source("<¶cie¿ka do pliku>/isowitreglog.r")`

* Skrypt oblicza regresje logistyczne dla zmiennych jako¶ciowych (factor)

Skrypty te dodatkowo generuj± w podkatalogu *rysunki*, który sam tworzy zrzuty wykresów w jpegach do pó¼niejszego przejrzenia.

Z poprzedniego postu:

* Dla ciekawych, gdzie prowadzi [**"bia³y królik"**](http://marcinbielak.blogspot.com/2009/05/r-jezyk-statystyczny-do-wizualizacji.html), polecam [diceTV film o R](http://www.youtube.com/watch?v=ZwYQPtU2Pa0), [*R journal*](http://journal.r-project.org/current.html), [filmkurs z Kanady](http://www.youtube.com/user/wildsc0p) oraz osza³amiaj±c± [bazê wykresów](http://addictedtor.free.fr/graphiques/), zamieszczam [spis funkcji zwi±zanych z regresj±](http://cran.r-project.org/doc/contrib/Ricci-refcard-regression.pdf) oraz [zbiór stron zwi±zanych z zagadnieniami zaimplementowanymi w R](http://cran.r-project.org/web/views/), w tym strona o [ekonometrii](http://cran.r-project.org/web/views/Econometrics.html), gdzie mo¿na poczytaæ o pakietach liniowej regresji.

