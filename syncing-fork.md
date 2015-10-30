To sync this fork from the upstream repo:

First check upstream is setup:
```
$ git remote -v
origin  git@github.com:mpatric/AppSales-Mobile.git (fetch)
origin  git@github.com:mpatric/AppSales-Mobile.git (push)
```

Nope, then add it:
```
$ git remote add upstream git@github.com:omz/AppSales-Mobile.git
$ git remote -v
origin  git@github.com:mpatric/AppSales-Mobile.git (fetch)
origin  git@github.com:mpatric/AppSales-Mobile.git (push)
upstream  git@github.com:omz/AppSales-Mobile.git (fetch)
upstream  git@github.com:omz/AppSales-Mobile.git (push)
```

Then fetch upstream changes:
```
$ git fetch upstream
...
Unpacking objects: 100% (5/5), done.
From github.com:omz/AppSales-Mobile
 * [new branch]      master     -> upstream/master
```

Checkout master locally and merge upstream changes:
```
$ git checkout master
Already on 'master'
Your branch is up-to-date with 'origin/master'.

$ git merge upstream/master
Merge made by the 'recursive' strategy.
 Classes/Report.m | 11 +++++++++++
 1 file changed, 11 insertions(+)
```

Then commit and push the changes.
