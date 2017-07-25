# Git "sandwich" example

One part of a file that is being maintained as its own file in one
place, but as a part of a file in another place. This solution shows
merge and rebase used to shuffle in and out the "chop in/out" commit
that chops off the beginning and the end of the file as changes are
either made in the small to merge into the big, or vice versa.

    0cfd569 HEAD@{0}: merge min-max: Fast-forward
    726491a HEAD@{1}: checkout: moving from min-max to master
    0cfd569 HEAD@{2}: rebase -i (finish): returning to refs/heads/min-max
    0cfd569 HEAD@{3}: rebase -i (pick): change in the middle originating in minimal branch
    726491a HEAD@{4}: rebase -i: fast-forward
    292dc53 HEAD@{5}: rebase -i: fast-forward
    746e80d HEAD@{6}: rebase -i (start): checkout HEAD~4
    0858b6a HEAD@{7}: checkout: moving from minimal to min-max
    0858b6a HEAD@{8}: commit: change in the middle originating in minimal branch
    273f946 HEAD@{9}: merge master: Merge made by the 'recursive' strategy.
    34a40dd HEAD@{10}: checkout: moving from master to minimal
    726491a HEAD@{11}: commit: more middle stuff
    292dc53 HEAD@{12}: checkout: moving from minimal to master
    34a40dd HEAD@{13}: merge master: Merge made by the 'recursive' strategy.
    6ceeda6 HEAD@{14}: checkout: moving from master to minimal
    292dc53 HEAD@{15}: commit: change in the middle
    746e80d HEAD@{16}: checkout: moving from minimal to master
    6ceeda6 HEAD@{17}: commit: chop in/out
    746e80d HEAD@{18}: checkout: moving from master to minimal
    746e80d HEAD@{19}: commit (initial): initial commit
