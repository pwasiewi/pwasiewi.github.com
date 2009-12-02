---
layout: default
title: Liniowa regresja - zmiany w skryptach
---

Zmieni�a si� struktura skrypt�w z [GitHub-u](http://github.com/pwasiewi) uzyskiwanych komend�:

`git clone git://github.com/pwasiewi/iso.git`

Tworzy ta komenda katalog iso, a w nim nowe skrypty umieszcza. Plik *isowitdatasets.r* jest tym razem headerem zawieraj�cym definicje zbior�w danych i ich domy�lne przetwarzanie np. dyskretyzacja, zescorowanie i specyficzne zbiory nazw atrybut�w do dalszego stosowania. Po zmodyfikowaniu na pocz�tku ka�dego z plik�w: *isowitoptimlm.r*, *isowitalterlm.r*, *isowitoptimklas.r*, *isowitreglog.r* �cie�ki do skryptu z ko�c�wk� "..../iso" zwanej dalej <�cie�ka do pliku>, uruchamiamy R i wpisujemy:

`source("<�cie�ka do pliku>/isowitoptimlm.r")` 

* Skrypt przetwarzaj�c permutacje zmiennych obja�niaj�cych (dla n od 1 do liczby wszystkich atrybut�w wej�ciowych) wybiera najlepsz� regresj� liniow� wed�ug parametru r-square R2 dopuszczaj�c regresje z wariancj� r�wnomiernie roz�o�on� st�d testy levena i bptest na heterowariancj�

`source("<�cie�ka do pliku>/isowitalterlm.r")`

* Skrypt por�wnuje alternatywne formy uzyskiwania najlepszej regresji z redukcj� atrybut�w lub i bez niej na podstawie kryteri�w AIC i BIC oraz Ridge

`source("<�cie�ka do pliku>/isowitoptimklas.r")`

* Skrypt znajduje stosuj�c permutacje atrybut�w o d�ugo�ci od 1 do liczby wszystkich atrybut�w wej�ciowych najlepszy klasyfikator dla metod rpart, J48, svm, ipredknn, lda, NaiveBayes

`source("<�cie�ka do pliku>/isowitreglog.r")`

* Skrypt oblicza regresje logistyczne dla zmiennych jako�ciowych (factor)

Skrypty te dodatkowo generuj� w podkatalogu *rysunki*, kt�ry sam tworzy zrzuty wykres�w w jpegach do p�niejszego przejrzenia.

Z poprzedniego postu:

* Dla ciekawych, gdzie prowadzi [**"bia�y kr�lik"**](http://marcinbielak.blogspot.com/2009/05/r-jezyk-statystyczny-do-wizualizacji.html), polecam [diceTV film o R](http://www.youtube.com/watch?v=ZwYQPtU2Pa0), [*R journal*](http://journal.r-project.org/current.html), [filmkurs z Kanady](http://www.youtube.com/user/wildsc0p) oraz osza�amiaj�c� [baz� wykres�w](http://addictedtor.free.fr/graphiques/), zamieszczam [spis funkcji zwi�zanych z regresj�](http://cran.r-project.org/doc/contrib/Ricci-refcard-regression.pdf) oraz [zbi�r stron zwi�zanych z zagadnieniami zaimplementowanymi w R](http://cran.r-project.org/web/views/), w tym strona o [ekonometrii](http://cran.r-project.org/web/views/Econometrics.html), gdzie mo�na poczyta� o pakietach liniowej regresji.

