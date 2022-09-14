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
