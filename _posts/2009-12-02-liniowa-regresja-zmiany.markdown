---
layout: default
title: Liniowa regresja - zmiany w skryptach
---

Zmieniła się struktura skryptów z [GitHub-u](http://github.com/pwasiewi) uzyskiwanych komendą:

`git clone git://github.com/pwasiewi/iso.git`

Tworzy ta komenda katalog iso, a w nim nowe skrypty umieszcza. Plik *isowitdatasets.r* jest tym razem headerem zawierającym definicje zbiorów danych i ich domyślne przetwarzanie np. dyskretyzacja, zescorowanie i specyficzne zbiory nazw atrybutów do dalszego stosowania. Po zmodyfikowaniu na początku każdego z plików: *isowitoptimlm.r*, *isowitalterlm.r*, *isowitoptimklas.r*, *isowitreglog.r* ścieżki do skryptu z końcówką "..../iso" zwanej dalej <ścieżka do pliku>, uruchamiamy R i wpisujemy:

`source("<ścieżka do pliku>/isowitoptimlm.r")` 

* Skrypt *isowitoptimlm.r* przetwarzając permutacje zmiennych objaśniających (dla n od 1 do liczby wszystkich atrybutów wejściowych) wybiera najlepszą regresję liniową według parametru r-square R2 dopuszczając regresje z wariancją równomiernie rozłożoną stąd testy levena i bptest na heterowariancję

`source("<ścieżka do pliku>/isowitalterlm.r")`

* Skrypt *isowitalterlm.r* porównuje alternatywne formy uzyskiwania najlepszej regresji z redukcją atrybutów lub i bez niej na podstawie kryteriów AIC i BIC oraz Ridge

`source("<ścieżka do pliku>/isowitoptimklas.r")`

* Skrypt *isowitoptimklas.r* znajduje stosując permutacje atrybutów o długości od 1 do liczby wszystkich atrybutów wejściowych najlepszy klasyfikator dla metod rpart, J48, svm, ipredknn, lda, NaiveBayes

`source("<ścieżka do pliku>/isowitreglog.r")`

* Skrypt *isowitreglog.r* oblicza regresje logistyczne dla zmiennych jakościowych (factor)

Skrypty te dodatkowo generują w podkatalogu *rysunki*, który sam tworzy zrzuty wykresów w jpegach do późniejszego przejrzenia.

Z poprzedniego postu:

* Dla ciekawych, gdzie prowadzi [**"biały królik"**](http://marcinbielak.blogspot.com/2009/05/r-jezyk-statystyczny-do-wizualizacji.html), polecam [diceTV film o R](http://www.youtube.com/watch?v=ZwYQPtU2Pa0), [*R journal*](http://journal.r-project.org/current.html), [filmkurs z Kanady](http://www.youtube.com/user/wildsc0p) oraz oszałamiającą [bazę wykresów](http://addictedtor.free.fr/graphiques/), zamieszczam [spis funkcji związanych z regresją](http://cran.r-project.org/doc/contrib/Ricci-refcard-regression.pdf) oraz [zbiór stron związanych z zagadnieniami zaimplementowanymi w R](http://cran.r-project.org/web/views/), w tym strona o [ekonometrii](http://cran.r-project.org/web/views/Econometrics.html), gdzie można poczytać o pakietach liniowej regresji.

