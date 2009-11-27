---
layout: default
title: Pages at GitHub
---

Na temat git [strona gitready](http://www.gitready.com/), [spo³eczna ksi±¿ka](http://book.git-scm.com/) oraz [wolnodostêpna ksi±¿ka ProGit book](http://progit.org/book/) oraz filmy [Linus on Git](http://www.youtube.com/watch?v=4XpnKHJAok8) oraz [Git intro](http://video.linuxfoundation.org/video/1516), z tym, ¿e ten ostatni najlepiej w Youtube siê prezentuje i trzeba siê pogodziæ z za bardzo skompresowanym d¼wiêkiem.

Strona g³ówna u¿ytkownika GitHub-u znajduje siê w repozytorium username.github.com, gdy¿ najpierw zak³adamy sobie konto, a potem tworzymy w³asne repozytoria np.: takie jak iso lub w³a¶nie np. pwasiewi.github.com

Dodatkowo polecam [opis wykonania strony na GitHubie](http://blog.envylabs.com/2009/08/publishing-a-blog-with-github-pages-and-jekyll/) z list± komend ¶ci±gaj±cych stronê www projektu po wykonaniu jej automatycznie przyciskiem na GitHubie:

`git clone git://github.com/pwasiewi/iso.git;
cd iso;
git symbolic-ref HEAD refs/heads/gh-pages; rm .git/index; git clean -fdx; git pull origin gh-pages`

Po tych komendach mo¿na git checkout master lub git checkout gh-pages prze³±czaæ siê miêdzy repozytoriami skryptów i strony projektu.

