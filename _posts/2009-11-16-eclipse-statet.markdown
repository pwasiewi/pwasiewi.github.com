---
layout: default
title: Statet plugin Eclipse - instalacja 
---

Instaluję pakiet eclipse-sdk z wszystkimi zależnościami np. na gentoo emerge eclipse-sdk. Następnie z katalogu /usr/lib64/eclipse-3.6 usuwam zawartość i kopiuję tam z [mirrora Eclipse] (http://www.mirrorservice.org/sites/download.eclipse.org/eclipseMirror/eclipse/downloads/drops/) wersję eclipse-sdk 3.5 np. [dla linux 64-bit](http://www.mirrorservice.org/sites/download.eclipse.org/eclipseMirror/eclipse/downloads/drops/R-3.5.1-200909170800/eclipse-SDK-3.5.1-linux-gtk-x86_64.tar.gz). Po przekopiowaniu zawartości pakietu do katalogu /usr/lib64/eclipse-3.6,umieszczam (jeśli nie mam) skrypt eclipse-3.6 z UBI w /usr/local/bin i wykonuję polecenie: 

`eclipse-3.6 -clean`

, które czyści historię z komputera, na którym kompilowano eclipse-sdk.
Poprzez Help->Install New Software dopisuję strony update pluginów eclipse-sdk, najpierw [Egit](http://github.com/guides/using-the-egit-eclipse-plugin-with-github): http://www.jgit.org/updates, a potem [Statet](http://www.walware.de/goto/statet): http://download.walware.de/eclipse-3.5, po każdym dopisaniu zaznaczam biblioteki i narzędzia w lewym oknie i wykonuję Next, a następnie update, czasami z zaznaczeniem licencji: I Agree.

W katalogu roboczym eclipse (domyślnie /home/username/workspace) wykonuję:

`git clone git://github.com/pwasiewi/iso.git`

Uzyskuję katalog iso ze skryptami, następnie uruchamiam New->R-Project i nazywam go tak samo jak poprzedni katalog czyli iso. Po przycisku Finish pokazują się w folderze projektu iso sklonowane wcześniej pliki. Jeszcze dodaję do Windows->Preferences->StatET->Run/Debug->R-environment katalog "/usr/lib64/R" oraz "64bit". Po zdefiniowaniu w Run->Run Configurations->Rconsole new environment i uruchomieniu go uzyskuję w konsoli na dole R-shell oraz mogę zaznaczając tekst myszą poprzez Ctrl-R Ctrl-R wykonywać go w tej konsoli lub też wykonywać całe skrypty. Resztę udogodnień można doczytać w [manualu StatET](http://www.splusbook.com/Rintro/R_Eclipse_StatET.pdf).

Dodatkowe kursy języka R na [stronie R cources](http://www.splusbook.com/Rintro/RCourseMaterial.html) oraz wstęp po polsku [w publikacji Komsty](http://cran.r-project.org/doc/contrib/Komsta-Wprowadzenie.pdf).
