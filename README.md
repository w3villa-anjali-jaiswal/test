
PRACTICAL WORK



anjali@anjali-w3villa:~$ ls

blog_crud        Downloads         mst.pdf            Pictures  Templates
blog_ruby        gamejs            Music              Public    Videos
calculator-main  json-product-crd  news_api_js        ruby
Desktop          json-searchbar    node_modules       snap
Documents        login_page        package-lock.json  task-4

anjali@anjali-w3villa:~$ mkdir test

anjali@anjali-w3villa:~/test$ touch index.html

anjali@anjali-w3villa:~/test$ nano index.html

anjali@anjali-w3villa:~/test$ git status

On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	index.html

nothing added to commit but untracked files present (use "git add" to track)
anjali@anjali-w3villa:~/test$ git add index.html

anjali@anjali-w3villa:~/test$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   index.html

anjali@anjali-w3villa:~/test$ git commit -m "Add index.html file"
[master (root-commit) 26cb753] Add index.html file
 1 file changed, 1 insertion(+)
 create mode 100644 index.html

anjali@anjali-w3villa:~/test$ git remote add origin git@github.com:w3villa-anjali-jaiswal/test.git

anjali@anjali-w3villa:~/test$ git status 
On branch master
nothing to commit, working tree clean
anjali@anjali-w3villa:~/test$ git push -u origin main
error: src refspec main does not match any
error: failed to push some refs to 'git@github.com:w3villa-anjali-jaiswal/test.git'

anjali@anjali-w3villa:~/test$ git push -u origin main

error: src refspec main does not match any
error: failed to push some refs to 'git@github.com:w3villa-anjali-jaiswal/test.git'
anjali@anjali-w3villa:~/test$ git remote add origin git@github.com:w3villa-anjali-jaiswal/test.git
fatal: remote origin already exists.
anjali@anjali-w3villa:~/test$ git branch -M main
anjali@anjali-w3villa:~/test$ git push -u origin main

Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 245 bytes | 245.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:w3villa-anjali-jaiswal/test.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.



git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   index.html


 git add index.html
anjali@anjali-w3villa:~/test$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   index.html



anjali@anjali-w3villa:~/test$ nano index.html
anjali@anjali-w3villa:~/test$ git add index.html
anjali@anjali-w3villa:~/test$ git commit -m message"changed"

[main f9c233e] messagechanged
 1 file changed, 1 insertion(+), 1 deletion(-)

anjali@anjali-w3villa:~/test$ git push origin main

Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 279 bytes | 279.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:w3villa-anjali-jaiswal/test.git
   26cb753..f9c233e  main -> main


anjali@anjali-w3villa:~/test$ touch demo.html
anjali@anjali-w3villa:~/test$ nano demo.html

anjali@anjali-w3villa:~/test$ git add demo.html
anjali@anjali-w3villa:~/test$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   demo.html

File is now restore   

anjali@anjali-w3villa:~/test$ nano demo.html
anjali@anjali-w3villa:~/test$ git restore demo.html

anjali@anjali-w3villa:~/test$ git log
commit 2b91a572b01d206f47e9cd0c68a8f6bd4299b28c (HEAD -> main)
Author: ANJALI JAISWAL <anjali.jaiswal@w3villa.com>
Date:   Sat May 13 16:13:31 2023 +0530

    messagedemo

commit f9c233e2348ac9b054c4af59c5aad79adf263745
Author: ANJALI JAISWAL <anjali.jaiswal@w3villa.com>
Date:   Sat May 13 15:47:59 2023 +0530

    messagechanged

commit 26cb7535b8e75b6fd5c56dce2e89fb4613bf0edc
Author: ANJALI JAISWAL <anjali.jaiswal@w3villa.com>
Date:   Sat May 13 15:20:28 2023 +0530

    Add index.html file
anjali@anjali-w3villa:~/test$ git reset 26cb7535b8e75b6fd5c56dce2e89fb4613bf0edc
Unstaged changes after reset:
M	index.html
anjali@anjali-w3villa:~/test$ git status
On branch main
Your branch is behind 'origin/main' by 3 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	demo.html
	third.txt

no changes added to commit (use "git add" and/or "git commit -a")
anjali@anjali-w3villa:~/test$ git add index.html
anjali@anjali-w3villa:~/test$ git commit -m "after resettig"
[main 0ef635e] after resettig
 1 file changed, 1 insertion(+), 1 deletion(-)

anjali@anjali-w3villa:~/test$ git push origin main
To github.com:w3villa-anjali-jaiswal/test.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'git@github.com:w3villa-anjali-jaiswal/test.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

anjali@anjali-w3villa:~/test$ git push origin main -f
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 278 bytes | 278.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:w3villa-anjali-jaiswal/test.git
 + 8ddfd1b...0ef635e main -> main (forced update)
