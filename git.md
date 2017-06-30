# Getting to know Git more (undoing changes)
When I started with the minor Everything Web that's when I **really** began using Git and Github. I had used Github before but only to push something that was already finished.

After a few months really using Git, I knew the bare basics like `git add`, `git commit`, `git push` and `git merge` (also some commands for branches) but that was it. When something went wrong or when some action had to be reversed I would freak out and bang my head on the table (figuratively speaking) because I didn't know how to solve the problem and sometimes I ended up deleting a repo (if the project was still in the first phase) and adding it again. I still don't have enough knowledge about Git to feel comfortable with it.

So I decided to write an article about Git, a kind of tiny intermediate course to take a closer look at undoing actions. Not just to help you but also to help me become a better Git-user (or Gitter? However you want to call it) and to not freak out anymore when something goes south. If you don't know git command line at all I suggest watching [c0deporn's video](https://www.youtube.com/watch?v=Y9XZQO1n_7c) about the basics of git before proceeding with this article.

## How to undo changes
### File changes
For example, you've made some changes to your file and you've saved and closed the file afterwards. You realize that you've made a mistake and want to undo them. How would you do it?

First of all you need to view the changes made to check out if our changes are there. With `git diff` you can view lines of code that have been edited, added or removed (Micheal Hartl). If you decide that that's what you have changed and you want to undo it then you can use `git checkout -- <file>`, <file> is the name of the file you want to change (Kevin Skoglund).

After executing this command, your last changes will be removed!

### Undoing a `git add`
I once made a mistake with staging some files that belonged in the .gitignore. Boom! Banged my head on the table. So now what? I didn't read anything else inside the terminal (because let's be honest, hierarchy isn't really present) and if you don't read like me, you would be missing the obvious clue git gives us after using `git add`. It says: `use "git reset HEAD <file>" to unstage`, `HEAD` referring to the latest changes. That's it! all you have to do is replace <file> with the file name you want unstage and your crisis is over.

### Undoing a `git commit`
Undoing a commit is a lot harder than what I've talked about before, because every commit depends on the commit that went before it. Trying to change an older commit is tricky and shouldn't be done. However you could reverse the last commit and bring it back to the staging phase by executing `git commit --amend`. It will also try to make a new commit so you can change the message and add a file to the same commit (Danny Markov).

If you still need to change an older commit you can use `git revert <commit-id>` or when you just want to bring back the last commit to the staging phase without immediately committing it again you can use `git revert HEAD`. Every commit Git creates an id for the commit. With the id of a commit you can view changes made and in Github you can use it anywhere to refer back to that commit. The id is also crucial for reversing a commit. With `git log` you'll get a list of last commits and their id's. Use this id to execute `git revert`. **Remember that reversing older commits can cause problems and merge conflicts and isn't adviced** (Danny Markov).

### Undoing multiple commits
If you're working on a repo and you have changed something a view commits back and you want to go back to that point there is a command called `git reset`. `git reset` has three ways it can be executed, each of them a bit different.

#### `git reset --soft <commit-id>`
If you execute this command you will go back to a given commit without changing the staging index (files you already added to the staging area) or the working directory (Kevin Skoglund). So you keep all your changes up until the latest commit. The changes will then be seen as new changes and these will be automatically staged. You can also use reset to go back to the latest commit.

#### `git reset --mixed <commit-id>` (default)
If you execute this command it will change the staging index but it will keep the working directory untouched (Kevin Skoglund). In other words, every file will be the same as it was in the latest commit but it won't add those changes to the staging area. After resetting you will see the filename with a red font color when executing `git status`.

#### `git reset --hard <commit-id>`
This command is the most radical to execute and must be used with caution because both the staging index as the working directory will be changed until the given commit. Everything that comes after that commit will be gone (Kevin Skoglund). But you can still go to a future commit if you know the commit id.

### Final word
There is so much more to tell about Git but for now I hope you understand Git a bit better especially if your just starting and know the mistakes I've made all too well.

## Sources
1. Skoglund, K. (no date). *Git Essential Training*. Source:
https://www.lynda.com/Git-tutorials/Git-Essential-Training/100222-2.html
2. Hartl, M. (no date). *Learn enough Git to be dangerous*. Source:
https://www.learnenough.com/git-tutorial
3. Danny Markov. (June 2, 2016). *Learn Git in 30 Minutes*. Source: https://tutorialzine.com/2016/06/learn-git-in-30-minutes
