---
layout: default
title: Pages at GitHub
---

Na temat git [strona gitready](http://www.gitready.com/), [spo�eczna ksi��ka](http://book.git-scm.com/) oraz [wolnodost�pna ksi��ka ProGit book](http://progit.org/book/) oraz filmy [Linus on Git](http://www.youtube.com/watch?v=4XpnKHJAok8) oraz [Git intro](http://video.linuxfoundation.org/video/1516), z tym, �e ten ostatni najlepiej w Youtube si� prezentuje i trzeba si� pogodzi� z za bardzo skompresowanym d�wi�kiem.

Strona g��wna u�ytkownika GitHub-u znajduje si� w repozytorium username.github.com, gdy� najpierw zak�adamy sobie konto, a potem tworzymy w�asne repozytoria np.: takie jak iso lub w�a�nie np. pwasiewi.github.com

Dodatkowo polecam [opis wykonania strony na GitHubie](http://blog.envylabs.com/2009/08/publishing-a-blog-with-github-pages-and-jekyll/) z list� komend �ci�gaj�cych stron� www projektu po wykonaniu jej automatycznie przyciskiem na GitHubie:

`git clone git://github.com/pwasiewi/iso.git;
cd iso;
git symbolic-ref HEAD refs/heads/gh-pages; rm .git/index; git clean -fdx; git pull origin gh-pages`

Po tych komendach mo�na git checkout master lub git checkout gh-pages prze��cza� si� mi�dzy repozytoriami skrypt�w i strony projektu.

