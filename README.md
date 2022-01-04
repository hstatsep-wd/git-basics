# Git Basics

## Before we begin

Note that there are a few ways you can work on a repository that is created on Github:
* Someone else can make the repo and give you access (like this one)
* You can make a brand new repo
* You can fork someone else's repo

## Getting started

1. Make sure you cd into the right folder first: `cd ~/wd/classwork` (think about this command; I won't always give it to you)
2. Now clone it: `git clone URL` (make sure you don't type `URL`, use your own URL).
3. Make sure you're in the habit of doing `cd REPONAME` after you clone!
4. Then open this `README.md` file in your IDE.

## Practicing the git flow

Remember, the usual flow is to **edit** --> **add** --> **commit** --> **push**. Let's try it!
Go ahead and type your first name on this line below. Replace the `X` with your name.

My first name is X.

Great! You made an edit! 
In your terminal, type the command you see below. Don't copy/paste it.
You'll want to have it memorized, and the way you memorize it is by typing it:

git status

See how the README is red? That means there are new changes that have NOT been staged yet.
Let's go ahead and stage them so that they are ready for the commit:

git add .

Awesome! Now type this command again, or press the up-arrow twice in your command line:

git status

See how the README is green? That means the file is "on the stage," so it will be included when we do a commit!
Let's go ahead and do a commit:

git commit -m "add first name"

Sweet! For proof that it worked, you can type this command:

git log

Remember, to get out of git log, press q to quit. 
Let's go ahead and push it with this command:

git push

If you reload the repo on Github.com, you should see your name in the README file!

Alright, first commit done. Let's have some more fun.
Here in the file editor, on the line below, replace the X with your last name:

My last name is X.

Now try this command in your terminal:

base64 /dev/urandom | head -c 100 > favorites.txt

Do you see a new file called favorites.txt in your file tree? Go ahead and open it.
Ah! It looks like someone threw up in that file! If you ask me, that file is NOT ready for a commit.
Let's ask git what the status of our files is:

git status

Ok, so we have two files with changes. Luckily, we don't have to add ALL files to the stage for a commit.
Let's add JUST the README to the stage:

git add README.md

Now try this command again (or up-arrow twice!):

git status

See how README.md is green and favorites.txt is red? That means ONLY the README will be committed, but favorites won't!
This is super helpful when you're working on multiple files and maybe some aren't at a good stopping point yet.
Let's go ahead and commit whatever is on the stage:

git commit -m "add last name"

At this point, we COULD push. But let's not. You don't ALWAYS have to push your code to Github.
Sometimes you might want to make multiple commits before pushing.
Let's go ahead and fix favorites.txt. Get rid of all that gross text and type some of your favorite things in it.
Remember, git status is your friend. So consider using it frequently!
At this point, hopefully you're getting used to this git workflow.
Go ahead and add and commit. This time, you decide a commit message that makes sense!

Great! Let's get a status report from our trusty friend:

git status

Awesome! We have two commits here locally that we're ready to push! Go ahead:

git push

Fantastic. Now you're on your own.
Make a new file named whatever you want (feel free to put text in it), then add/commit/push it!

You're all done! You're git-ting really good at this! 😉
