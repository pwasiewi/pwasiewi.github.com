---
layout: default
title: Statet plugin Eclipse - instalacja 
---

Instaluj� pakiet eclipse-sdk z wszystkimi zale�no�ciami np. na gentoo emerge eclipse-sdk. Nast�pnie z katalogu /usr/lib64/eclipse-3.6 usuwam zawarto�� i kopiuj� tam z [mirrora Eclipse] (http://www.mirrorservice.org/sites/download.eclipse.org/eclipseMirror/eclipse/downloads/drops/) wersj� eclipse-sdk 3.5 np. [dla linux 64-bit](http://www.mirrorservice.org/sites/download.eclipse.org/eclipseMirror/eclipse/downloads/drops/R-3.5.1-200909170800/eclipse-SDK-3.5.1-linux-gtk-x86_64.tar.gz). Po przekopiowaniu zawarto�ci pakietu do katalogu /usr/lib64/eclipse-3.6,umieszczam (je�li nie mam) skrypt eclipse-3.6 z UBI w /usr/local/bin i wykonuj� polecenie: 

`eclipse-3.6 -clean`

, kt�re czy�ci histori� z komputera, na kt�rym kompilowano eclipse-sdk.
Poprzez Help->Install New Software dopisuj� strony update plugin�w eclipse-sdk, najpierw [Egit](http://github.com/guides/using-the-egit-eclipse-plugin-with-github): http://www.jgit.org/updates, a potem [Statet](http://www.walware.de/goto/statet): http://download.walware.de/eclipse-3.5, po ka�dym dopisaniu zaznaczam biblioteki i narz�dzia w lewym oknie i wykonuj� Next, a nast�pnie update, czasami z zaznaczeniem licencji: I Agree.

W katalogu roboczym eclipse (domy�lnie /home/username/workspace) wykonuj�:

`git clone git://github.com/pwasiewi/iso.git`

Uzyskuj� katalog iso ze skryptami, nast�pnie uruchamiam New->R-Project i nazywam go tak samo jak poprzedni katalog czyli iso. Po przycisku Finish pokazuj� si� w folderze projektu iso sklonowane wcze�niej pliki. Jeszcze dodaj� do Windows->Preferences->StatET->Run/Debug->R-environment katalog "/usr/lib64/R" oraz "64bit". Po zdefiniowaniu w Run->Run Configurations->Rconsole new environment i uruchomieniu go uzyskuj� w konsoli na dole R-shell oraz mog� zaznaczaj�c tekst mysz� poprzez Ctrl-R Ctrl-R wykonywa� go w tej konsoli lub te� wykonywa� ca�e skrypty. Reszt� udogodnie� mo�na doczyta� w [manualu StatET](http://www.splusbook.com/Rintro/R_Eclipse_StatET.pdf).

Dodatkowe kursy j�zyka R na [stronie R cources](http://www.splusbook.com/Rintro/RCourseMaterial.html) oraz wst�p po polsku [w publikacji Komsty](http://cran.r-project.org/doc/contrib/Komsta-Wprowadzenie.pdf).
