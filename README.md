# driftnoise

* mapborealis presentation and info [http://www.math.uni-bremen.de/zetem/cms/detail.php?id=21687](http://www.math.uni-bremen.de/zetem/cms/detail.php?id=21687)
* projects, e.g. https://driftnoise.com/fastcast2.html
* dropbox docs
* "DLR will perform ice drift forecast validations, using their newly developed algorithm based on the **phase correlation method for high-resolution ice drift tracing**, from Sentinel-1 image pairs." (FastCast II)

### Git Tips
* [https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
* [https://cbea.ms/git-commit/](https://cbea.ms/git-commit/)
    * set commit message template [https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration)
* [https://xdg.me/a-survey-of-git-best-practices/](https://xdg.me/a-survey-of-git-best-practices/)

### Git Rebase

* `git status`
* `git diff`
* `git commit`
* `git commit -a` its like an add+commit
* `git log`
* `git rebase -i specify-gdal-headers~3` do an interactive rebase on that branch, go three commits back. Instructions are shown in the editor, (`pick`, `squash` (like done here) etc.), then in case of squash the commit message could be altered afterwards
* `git log`
* `git commit --amend` change the commit msg of last commit in case of typo
* `git push` fails in this case, because history on origin is different
* `git push --force-with-lease` force push but notify other ppl working on the branch

* `git push -u origin branch` push local branch thats never been pushed to origin

If a rebase goes wrong and needs to be reset
* `git rebase --abort`
* `git reset --hard origin/new_greenland`

If merging conflicts cant be resolved with git
* sometimes its good to use tig for an overview (enter/q)
* during the merge conflict the arctic.json was overwritten again, then it worked (just dropped unneccesary commits til last one, led to merge error, overwrite json, git add json-datei, git rebase --continue and that worked

* to push branch that only exists locally mention its name `git push origin <local_branch>`

* `branch -m b1 b2` to move branch 1 to branch 2 (e.g. delete branch 2 beforehand, `git branch -D <branch>`)
* `git log -S 'bla'` look for commits that had something to do with 'bla', like a specific blame
* `git config --global --edit`

* `git pull --rebase` when rebased online and changes can'T be fast-forwarded

### vim

* dd zeile löschen
* . kommando wiederholen
* / suchen
* n suche wiederholen

### grep
* surpress error msg when using `grep`: `grep -r "priima" / 2>&-`

### pattern matching
* beim kopieren etc. einfach `[0-9]` etc. um genaueres anzugeben als wildcard

### geojson land mask
* simplify with `sf_simplify`, cut decimal points with `ogr2ogr -f GeoJSON -lco COORDINATE_PRECISION=4 less_magic.geojson magic.geojson`

### debugging
* zb mit `gdb --args` ..und dann der function call, danach `run` eingeben
