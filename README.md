# Gym Git Exercise Solutions
## Bundle1
### Exercse1
```bash
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git init
Initialized empty Git repository in C:/Users/User/Music/Gym-Git-Exercise-Solution/.git/
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git branch -M main
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch main

No commits yet

Untracked files:
        README.md

nothing added to commit but untracked files present (use "git add" to track)
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md

[main (root-commit) 103adc0] add Readme file
 1 file changed, 3 insertions(+)
 create mode 100644 README.md
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git remote add origin https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Writing objects: 100% (3/3), 261 bytes | 130.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout -b test
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout dev
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push --set-upstream origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/devfabien/Gym-Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
 * [new branch]      dev -> dev
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout test
Switched to branch 'test'
fatal: The current branch test has no upstream branch.

    git push --set-upstream origin test

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push --set-upstream origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/devfabien/Gym-Git-Exercise-Solutions/pull/new/test
remote:
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
 * [new branch]      test -> test
branch 'test' set up to track 'origin/test'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git branch -D test
Deleted branch test (was 103adc0).
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push origin --delete test
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
 - [deleted]         test
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> 
```
### Exercise2
```bash
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add home.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git stash
Saved working directory and index state WIP on dev: 103adc0 add Readme file
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git stash list
stash@{0}: WIP on dev: 103adc0 add Readme file
Your branch is up to date with 'origin/dev'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add about.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git stash
Saved working directory and index state WIP on dev: 103adc0 add Readme file
Your branch is up to date with 'origin/dev'.

  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add team.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git stash list
stash@{0}: WIP on dev: 103adc0 add Readme file
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
Your branch is up to date with 'origin/dev'.

Changes to be committed:
        new file:   team.html

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git stash
Saved working directory and index state WIP on dev: 103adc0 add Readme file
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git stash list
stash@{0}: WIP on dev: 103adc0 add Readme file
stash@{1}: WIP on dev: 103adc0 add Readme file
stash@{2}: WIP on dev: 103adc0 add Readme file
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (cc60ee6fecc614175ed0ec303107bd028e5f035c)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution>git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (50595b11b2e1174761469ffa62a7ee537bc3153d)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add .
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "add home and about page"
[dev 2a0e35e] add home and about page
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
Counting objects: 100% (5/5), done.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 550 bytes | 137.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
   103adc0..2a0e35e  dev -> dev
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git stash list
stash@{0}: WIP on dev: 103adc0 add Readme file
PS C:\Users\User\Music\Gym-Git-Exercise-Solution>git stash pop 

On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (0c7962f1e4082ef8cf8b5e0a8d208ebfe8ed14c0)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git reset --hard
HEAD is now at 2a0e35e add home and about page
PS C:\Users\User\Music\Gym-Git-Exercise-Solution>

```
## Bundle2
### Exercise1

```bash
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        service.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add .
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "add service page"
[ft/bundle-2 ae16721] add service page
 1 file changed, 12 insertions(+)
 create mode 100644 service.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.    
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done. 
Writing objects: 100% (3/3), 462 bytes | 231.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/devfabien/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> 

```
## Exercise2
 ```bash
Your branch is up to date with 'origin/main'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git pull
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 625 bytes | 4.00 KiB/s, done.
From https://github.com/devfabien/Gym-Git-Exercise-Solutions
   103adc0..83d089b  main       -> origin/main
Updating 103adc0..83d089b
Fast-forward
 about.html   | 12 ++++++++++++
 service.html | 12 ++++++++++++
 3 files changed, 36 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 service.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   service.html

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add .
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "add webdeveloper service"
 1 file changed, 1 insertion(+)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 339 bytes | 169.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/devfabien/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout main
Your branch is up to date with 'origin/main'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   service.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add .
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "add webhosting service"
[main 2b286da] add webhosting service
 1 file changed, 1 insertion(+)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 333 bytes | 166.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git merge main
Auto-merging service.html
CONFLICT (content): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status 
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   service.html

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   service.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
Your branch is up to date with 'origin/ft/service-redesign'.

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   service.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   service.html

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add .
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   service.html

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "add service list"
[ft/service-redesign f9d2bdc] add service list
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 327 bytes | 163.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
   ff14497..f9d2bdc  ft/service-redesign -> ft/service-redesign
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> 
 ```
 ### Bundle3
 ## Exercise1
  ```bash
  PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add .
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "add team page"
[ft/team-page 966fd5b] add team page
 create mode 100644 team.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
To push the current branch and set the remote as upstream, use
    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\User\Music\Gym-Git-Exercise-Solution>  git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 455 bytes | 227.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/devfabien/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git log
Author: devfabien <ish001fabi@gmail.com>

    add team page

commit f9d2bdcc9afecdbe9751902b1d6c2023a439a488 (origin/ft/service-redesign, ft/service-redesign)
Author: devfabien <ish001fabi@gmail.com>
Date:   Sun May 21 09:16:25 2023 -0700

    add service list

commit 2b286dada13d23ae9f205bc62d05e8fd804f0ebc (origin/main, main, ft/contact-page)

    add webhosting service

Author: devfabien <ish001fabi@gmail.com>
Date:   Sun May 21 09:06:42 2023 -0700

    add webdeveloper service

commit 83d089bf7fb0fc2765ceaf6b868e8a9ef24732fd
Merge: 103adc0 ae16721
Author: Fabien I <119418479+devfabien@users.noreply.github.com>
Date:   Sun May 21 09:02:41 2023 -0700
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout ft/contact-page
Switched to branch 'ft/contact-page'
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git cherry-pick 966fd5b4b4aa1d377a2847cb7a9fdfa4a68509f7
[ft/contact-page 1bd6271] add team page
 Date: Sun May 21 09:21:25 2023 -0700
 create mode 100644 team.html
On branch ft/contact-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        contact.html

nothing added to commit but untracked files present (use "git add" to track)
[ft/contact-page 03beabf] add contact page
 1 file changed, 12 insertions(+)
 create mode 100644 contact.html
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 717 bytes | 239.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/devfabien/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
Revert "add team page"
Switched to a new branch 'ft/faq'
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch ft/faq
  (use "git add <file>..." to include in what will be committed)
        faq.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add .
[ft/faq a1bd383] add faq page
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push --set-upstream origin ft/faq 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 449 bytes | 224.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq' on GitHub by visiting:
remote:      https://github.com/devfabien/Gym-Git-Exercise-Solutions/pull/new/ft/faq
remote:
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq -> ft/faq
branch 'ft/faq' set up to track 'origin/ft/faq'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git revert 966fd5b4b4aa1d377a2847cb7a9fdfa4a68509f7
[ft/faq 4a23301] Revert "add team page"
 1 file changed, 12 deletions(-)
 delete mode 100644 team.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch ft/faq
Your branch is ahead of 'origin/ft/faq' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 265 bytes | 132.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
   a1bd383..4a23301  ft/faq -> ft/faq
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> 
  ```
  ## Exercise2
```bash
PS C:\Users\User\Music\Gym-Git-Exercise-Solution>git checkout ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git restore <file>..." to discard changes in working directory)

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add .
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "add homepage latest news"
[main 47a3681] add homepage latest news
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 325 bytes | 162.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
   2b286da..47a3681  main -> main
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch ft/home-page-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add .
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "add homepage article"
[ft/home-page-redesign fa6decc] add homepage article
 1 file changed, 1 insertion(+)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 4 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.53 KiB | 142.00 KiB/s, done.
Total 14 (delta 7), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (7/7), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/devfabien/Gym-Git-Exercise-Solutions/pull/new/ft/home-page-redesign
remote:
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution>
```
## Bundle4
### Exercise1
```bash
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git remote add git-copy https://github.com/devfabien/Gym-Git-exercise-clone.git
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add.
git: 'add.' is not a git command. See 'git --help'.

The most similar command is
        add
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add .
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "adding new features"
[main d549dbc] adding new features
 1 file changed, 1 insertion(+)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push origin
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 325 bytes | 162.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
   47a3681..d549dbc  main -> main
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push git-copy
Enumerating objects: 20, done.
Counting objects: 100% (20/20), done.
Delta compression using up to 4 threads
Compressing objects: 100% (19/19), done.
Writing objects: 100% (20/20), 2.37 KiB | 303.00 KiB/s, done.
Total 20 (delta 9), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (9/9), done.
To https://github.com/devfabien/Gym-Git-exercise-clone.git
 * [new branch]      main -> main
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> 
```
### Exercise2

 ```bash
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout main
Switched to branch 'main'
Switched to a new branch 'ft/footer'
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch ft/footer
Untracked files:
  (use "git add <file>..." to include in what will be committed)

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "add footer page"
[ft/footer 25f2917] add footer page
 1 file changed, 12 insertions(+)
 create mode 100644 footer.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch ft/footer
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
        modified:   footer.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add footer.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch ft/footer
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   footer.html

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "add footer content"
[ft/footer 3ec6d82] add footer content
 1 file changed, 1 insertion(+)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
To push the current branch and set the remote as upstream, use


upstream, see 'push.autoSetupRemote' in 'git help config'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push --set-upstream origin ft/footer
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 716 bytes | 238.00 KiB/s, done.
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/devfabien/Gym-Git-Exercise-Solutions/pull/new/ft/footer
remote:
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout main
Your branch is up to date with 'origin/main'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout -b ft/squashing
fatal: a branch named 'ft/squashing' already exists
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout ft/squashing   
Switched to branch 'ft/squashing'
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git merge --squash ft/footer
Updating d549dbc..3ec6d82
Fast-forward
 footer.html | 13 +++++++++++++
 1 file changed, 13 insertions(+)
 create mode 100644 footer.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git status
On branch ft/squashing
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   footer.html

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "footer changes squashing"
[ft/squashing 38a4bab] footer changes squashing
 1 file changed, 13 insertions(+)
 create mode 100644 footer.html
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
fatal: The current branch ft/squashing has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/squashing

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push --set-upstream origin ft/squashing
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 462 bytes | 231.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/devfabien/Gym-Git-Exercise-Solutions/pull/new/ft/squashing
remote:
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> 
 ```
 ## Bundle5

 ### Excercise1

 ```bash
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    home.html

Untracked files:
        index.html
no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git add .
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git  status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    home.html -> index.html

PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git commit -m "rename home to index"
[main 869964e] rename home to index
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename home.html => index.html (100%)
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 233 bytes | 46.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/devfabien/Gym-Git-Exercise-Solutions.git
   d549dbc..869964e  main -> main
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git pull
Already up to date.
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> git push git-copy
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 233 bytes | 116.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/devfabien/Gym-Git-exercise-clone.git
   d549dbc..869964e  main -> main
PS C:\Users\User\Music\Gym-Git-Exercise-Solution> 
 ```
 ### Exercise2

 ```bash 
PS C:\Users\User\Music\git-cafe-exercise> git status
On branch main
Your branch is up to date with 'origin/main'.
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\User\Music\git-cafe-exercise> git add index.html
PS C:\Users\User\Music\git-cafe-exercise> git status
Your branch is up to date with 'origin/main'.

  (use "git restore --staged <file>..." to unstage)
        modified:   index.html

PS C:\Users\User\Music\git-cafe-exercise> git commit -m "changing the welcome title"
[main dad4e57] changing the welcome title
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\User\Music\git-cafe-exercise> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 322 bytes | 11.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/devfabien/git-cafe-exercise.git
   d1d3f9c..dad4e57  main -> main
PS C:\Users\User\Music\git-cafe-exercise> 
 ```
 ## Bundle1
 ### Exercise1
 ```bash
PS C:\Users\User\Music\git-cafe-exercise> git checkout -b ft/menu
Switched to a new branch 'ft/menu'
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        menu.html
nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\User\Music\git-cafe-exercise> git add .
PS C:\Users\User\Music\git-cafe-exercise> git commit -m "add menu page"
[ft/menu 2c91226] add menu page
 1 file changed, 12 insertions(+)
 create mode 100644 menu.html
PS C:\Users\User\Music\git-cafe-exercise> git push --set-upstream origin ft/menu
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 459 bytes | 229.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/menu' on GitHub by visiting:
remote:      https://github.com/devfabien/git-cafe-exercise/pull/new/ft/menu
remote:
To https://github.com/devfabien/git-cafe-exercise.git
 * [new branch]      ft/menu -> ft/menu
branch 'ft/menu' set up to track 'origin/ft/menu'.
PS C:\Users\User\Music\git-cafe-exercise>
 ```
 ### Exercise2

```bash
PS C:\Users\User\Music\git-cafe-exercise> git status
On branch bug-fix/contact
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    index-4.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Contact.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\User\Music\git-cafe-exercise> git add .
PS C:\Users\User\Music\git-cafe-exercise> git status
On branch bug-fix/contact
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    index-4.html -> Contact.html

PS C:\Users\User\Music\git-cafe-exercise> git commit -m "rename index4 to Contact"
[bug-fix/contact 3cbae71] rename index4 to Contact
 1 file changed, 203 insertions(+), 203 deletions(-)
 rename index-4.html => Contact.html (97%)
PS C:\Users\User\Music\git-cafe-exercise> git push --set-upstream origin bug-fix/contact
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 2.49 KiB | 849.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'bug-fix/contact' on GitHub by visiting:
remote:      https://github.com/devfabien/git-cafe-exercise/pull/new/bug-fix/contact
remote:
To https://github.com/devfabien/git-cafe-exercise.git
 * [new branch]      bug-fix/contact -> bug-fix/contact
branch 'bug-fix/contact' set up to track 'origin/bug-fix/contact'.
PS C:\Users\User\Music\git-cafe-exercise>  
```
### Exercise3

```bash
PS C:\Users\User\Music\git-cafe-exercise> git checkout main
PS C:\Users\User\Music\git-cafe-exercise> git checkout -b hotfix/contact
Switched to a new branch 'hotfix/contact'
PS C:\Users\User\Music\git-cafe-exercise> git status
On branch hotfix/contact
Changes not staged for commit:
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index-4.html
no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\User\Music\git-cafe-exercise> git add .
PS C:\Users\User\Music\git-cafe-exercise> git status
On branch hotfix/contact
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index-4.html

PS C:\Users\User\Music\git-cafe-exercise> git commit -m "change hotfix contact"
[hotfix/contact 2b8b4b1] change hotfix contact
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\User\Music\git-cafe-exercise> git push --set-upstream origin hotfix/contact
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 295 bytes | 295.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'hotfix/contact' on GitHub by visiting:
remote:      https://github.com/devfabien/git-cafe-exercise/pull/new/hotfix/contact
remote:
To https://github.com/devfabien/git-cafe-exercise.git
 * [new branch]      hotfix/contact -> hotfix/contact
branch 'hotfix/contact' set up to track 'origin/hotfix/contact'.
PS C:\Users\User\Music\git-cafe-exercise> 
```