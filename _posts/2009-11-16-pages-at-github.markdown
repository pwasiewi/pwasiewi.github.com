---
layout: default
title: Pages at GitHub
---

Na temat git [strona gitready](http://www.gitready.com/), [społeczna książka](http://book.git-scm.com/) oraz [wolnodostępna książka ProGit book](http://progit.org/book/) oraz filmy [Linus on Git](http://www.youtube.com/watch?v=4XpnKHJAok8) oraz [Git intro](http://video.linuxfoundation.org/video/1516), z tym, że ten ostatni najlepiej w Youtube się prezentuje i trzeba się pogodzić z za bardzo skompresowanym dźwiękiem.

Strona główna użytkownika GitHub-u znajduje się w repozytorium username.github.com, gdyż najpierw zakładamy sobie konto, a potem tworzymy własne repozytoria np.: takie jak iso lub właśnie np. pwasiewi.github.com

Dodatkowo polecam [opis wykonania strony na GitHubie](http://blog.envylabs.com/2009/08/publishing-a-blog-with-github-pages-and-jekyll/) z listą komend ściągających stronę www projektu po wykonaniu jej automatycznie przyciskiem na GitHubie:

`git clone git://github.com/pwasiewi/iso.git;
cd iso;
git symbolic-ref HEAD refs/heads/gh-pages; rm .git/index; git clean -fdx; git pull origin gh-pages`

Po tych komendach można git checkout master lub git checkout gh-pages przełączać się między repozytoriami skryptów i strony projektu.

