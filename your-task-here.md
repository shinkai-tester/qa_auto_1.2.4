# This is task for you


<details>
  <summary>Click me or don't</summary><br/>
  do you like this markdown feature? :) <br/>
  ok, but let's proceed with the tasks
</details>

**Let's get started**

1. Do the fork of this repo to your github (yes, learn what is *fork*) and clone this your new repo to your local
2. Add 3 new .md files using for each of them separate commit (call them "first", "second", "third" to check it more easier later)
3. Learn how to use `git reset` ([help](https://git-scm.com/book/ru/v2/%D0%98%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D1%8B-Git-%D0%A0%D0%B0%D1%81%D0%BA%D1%80%D1%8B%D1%82%D0%B8%D0%B5-%D1%82%D0%B0%D0%B9%D0%BD-reset))
4. Try to reset your commits:
- first, check git logs using a specific command and get commits id's (preferably short versions of them)
- execute `git reset --soft bc9cfc7` (just replace the commit id with your second commit id) - you reset current HEAD to the second commit!
- check git logs (using git command) and check what happened with your code
- execute `git reset --soft hg455kj` (replace the commit id with your third commit id) - you changed back the HEAD to the third commit!
- check git logs (using git command) and check what happened with your code (magic!)
- do the same using 2 other parameters for `git reset` command
- write down and share with us what you have noticed in the code after using each of these 3 parameters
- save logs for all theese actions into a file and share it with us!

```bash
alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        first.md
        second.md
        third.md

nothing added to commit but untracked files present (use "git add" to track)

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git add first.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git commit -m "there is the 1st commit"
[main 3ab4fbe] there is the 1st commit
 1 file changed, 1 insertion(+)
 create mode 100644 first.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git add second.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git commit -m "there is the 2nd commit"
[main 2090e91] there is the 2nd commit
 1 file changed, 1 insertion(+)
 create mode 100644 second.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git add third.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git commit -m "there is the 3rd commit"
[main 82b147f] there is the 3rd commit
 1 file changed, 1 insertion(+)
 create mode 100644 third.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git log --graph --all --oneline
* 82b147f (HEAD -> main) there is the 3rd commit
* 2090e91 there is the 2nd commit
* 3ab4fbe there is the 1st commit
* 26b2d85 (origin/main, origin/HEAD) Update your-task-here.md
* 93e058d Update your-task-here.md
* 685ce8d Update README.md
* 047c466 Update your-task-here.md
* c2930aa Update your-task-here.md
* 05f3594 rename task file
* b85e79d add a task for students
* d2fa1c4 Create README.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git reset --soft 2090e91

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git log --graph --all --oneline
* 2090e91 (HEAD -> main) there is the 2nd commit
* 3ab4fbe there is the 1st commit
* 26b2d85 (origin/main, origin/HEAD) Update your-task-here.md
* 93e058d Update your-task-here.md
* 685ce8d Update README.md
* 047c466 Update your-task-here.md
* c2930aa Update your-task-here.md
* 05f3594 rename task file
* b85e79d add a task for students
* d2fa1c4 Create README.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   third.md


alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git reset --soft 82b147f

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git log --graph --all --oneline
* 82b147f (HEAD -> main) there is the 3rd commit
* 2090e91 there is the 2nd commit
* 3ab4fbe there is the 1st commit
* 26b2d85 (origin/main, origin/HEAD) Update your-task-here.md
* 93e058d Update your-task-here.md
* 685ce8d Update README.md
* 047c466 Update your-task-here.md
* c2930aa Update your-task-here.md
* 05f3594 rename task file
* b85e79d add a task for students
* d2fa1c4 Create README.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git reset 2090e91

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        third.md

nothing added to commit but untracked files present (use "git add" to track)

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git log --graph --all --oneline
* 2090e91 (HEAD -> main) there is the 2nd commit
* 3ab4fbe there is the 1st commit
* 26b2d85 (origin/main, origin/HEAD) Update your-task-here.md
* 93e058d Update your-task-here.md
* 685ce8d Update README.md
* 047c466 Update your-task-here.md
* c2930aa Update your-task-here.md
* 05f3594 rename task file
* b85e79d add a task for students
* d2fa1c4 Create README.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git reset 82b147f

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git log --graph --all --oneline
* 82b147f (HEAD -> main) there is the 3rd commit
* 2090e91 there is the 2nd commit
* 3ab4fbe there is the 1st commit
* 26b2d85 (origin/main, origin/HEAD) Update your-task-here.md
* 93e058d Update your-task-here.md
* 685ce8d Update README.md
* 047c466 Update your-task-here.md
* c2930aa Update your-task-here.md
* 05f3594 rename task file
* b85e79d add a task for students
* d2fa1c4 Create README.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git reset --hard 2090e91
HEAD is now at 2090e91 there is the 2nd commit

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git log --graph --all --oneline
* 2090e91 (HEAD -> main) there is the 2nd commit
* 3ab4fbe there is the 1st commit
* 26b2d85 (origin/main, origin/HEAD) Update your-task-here.md
* 93e058d Update your-task-here.md
* 685ce8d Update README.md
* 047c466 Update your-task-here.md
* c2930aa Update your-task-here.md
* 05f3594 rename task file
* b85e79d add a task for students
* d2fa1c4 Create README.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git reset --hard 82b147f
HEAD is now at 82b147f there is the 3rd commit

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git log --graph --all --oneline
* 82b147f (HEAD -> main) there is the 3rd commit
* 2090e91 there is the 2nd commit
* 3ab4fbe there is the 1st commit
* 26b2d85 (origin/main, origin/HEAD) Update your-task-here.md
* 93e058d Update your-task-here.md
* 685ce8d Update README.md
* 047c466 Update your-task-here.md
* c2930aa Update your-task-here.md
* 05f3594 rename task file
* b85e79d add a task for students
* d2fa1c4 Create README.md

alexa@Shinkai MINGW64 ~/IT_Switcher_JS/qa_auto_1.2.4 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```
