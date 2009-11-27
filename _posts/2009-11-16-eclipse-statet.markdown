---
layout: default
title: Statet plugin Eclipse - instalacja 
---

Instalujê pakiet eclipse-sdk z wszystkimi zale¿no¶ciami np. na gentoo emerge eclipse-sdk. Nastêpnie z katalogu /usr/lib64/eclipse-3.6 usuwam zawarto¶æ i kopiujê tam z [mirrora Eclipse] (http://www.mirrorservice.org/sites/download.eclipse.org/eclipseMirror/eclipse/downloads/drops/) wersjê eclipse-sdk 3.5 np. [dla linux 64-bit](http://www.mirrorservice.org/sites/download.eclipse.org/eclipseMirror/eclipse/downloads/drops/R-3.5.1-200909170800/eclipse-SDK-3.5.1-linux-gtk-x86_64.tar.gz). Po przekopiowaniu zawarto¶ci pakietu do katalogu /usr/lib64/eclipse-3.6,umieszczam (je¶li nie mam) skrypt eclipse-3.6 z UBI w /usr/local/bin i wykonujê polecenie: 

`eclipse-3.6 -clean`

, które czy¶ci historiê z komputera, na którym kompilowano eclipse-sdk.
Poprzez Help->Install New Software dopisujê strony update pluginów eclipse-sdk, najpierw [Egit](http://github.com/guides/using-the-egit-eclipse-plugin-with-github): http://www.jgit.org/updates, a potem [Statet](http://www.walware.de/goto/statet): http://download.walware.de/eclipse-3.5, po ka¿dym dopisaniu zaznaczam biblioteki i narzêdzia w lewym oknie i wykonujê Next, a nastêpnie update, czasami z zaznaczeniem licencji: I Agree.

W katalogu roboczym eclipse (domy¶lnie /home/username/workspace) wykonujê:

`git clone git://github.com/pwasiewi/iso.git`

Uzyskujê katalog iso ze skryptami, nastêpnie uruchamiam New->R-Project i nazywam go tak samo jak poprzedni katalog czyli iso. Po przycisku Finish pokazuj± siê w folderze projektu iso sklonowane wcze¶niej pliki. Jeszcze dodajê do Windows->Preferences->StatET->Run/Debug->R-environment katalog "/usr/lib64/R" oraz "64bit". Po zdefiniowaniu w Run->Run Configurations->Rconsole new environment i uruchomieniu go uzyskujê w konsoli na dole R-shell oraz mogê zaznaczaj±c tekst mysz± poprzez Ctrl-R Ctrl-R wykonywaæ go w tej konsoli lub te¿ wykonywaæ ca³e skrypty. Resztê udogodnieñ mo¿na doczytaæ w [manualu StatET](http://www.splusbook.com/Rintro/R_Eclipse_StatET.pdf).

Dodatkowe kursy jêzyka R na [stronie R cources](http://www.splusbook.com/Rintro/RCourseMaterial.html) oraz wstêp po polsku [w publikacji Komsty](http://cran.r-project.org/doc/contrib/Komsta-Wprowadzenie.pdf).
