# Task 1

There is a typo somewhere in markdown-text.md

From your machine, try to find out where the typo is.

(if you are on Ubuntu/similar)

`
nano LICENSE.md
`

(or whatever text editor you prefer)


Once you've found the typo, correct it. Now, you need to tell Git that you corrected the typo. 

How do we do that?

## Commits

> Matter is made of atoms, and repositories are made of commits.

Just like how an atom is the fundamental unit of matter, a commit is the fundamental unit of a repository.

A commit is a change - it literally is  "difference" between the past and the present.

Go back to the terminal and type 

`
git diff
`

You will see something like this: 

<img src="https://user-images.githubusercontent.com/32199592/98148787-08e45500-1ef3-11eb-8e43-69dd0c477b94.png" alt="diff-file.jpg"/>

git diff -> tells you what *changed*. 

In this case, change is measured between commits i.e. change between the last commit and whatever changes you just made.

If you type 

`
git log
`

You will see that there is already a commit in the repository and that commit is mine - when I created this project.
Whatever changes you bought after that commit is tracked by git - and this is what git does best - track changes!

So a commit is just a "change" that has some associated details with it - like who changed it & when. Observe carefully the results of `git log` - the first commit says my name and also the date when I created the commit along with a 'message'. 

This is very useful when you have a lot of people working on the same project and if you ever feel the need to go back to a certain time in the past when you wish you hadn't written a piece of code - you can do that with Git! But more on that, later.

## Creating a commit

Now that you know what a commit is, let's learn how to create one yourself.

Once you're happy with your changes, type

`
git add LICENSE.md
`

The file isn't commit-ed yet (apparent from the output of `git log`) but an interesting thing happens now - if you type `git diff` - your change or your "diff" is not visible anymore.

What `git add` does is it adds your file to a "staging area" or a "preparation area" - think of it as a queue - you just changed something and the next step is commit-ing.

`
git commit LICENSE.md -m "task1: Correct typo"
`

As I said earlier, each commit is associated with its own set of details. One of the details is a message, and that is what the `-m` option does - these are called "commit messages" and you want your commit messages to be as clear as possible. Observe the format I followed for my commit message:

`task1:` I'm specifying which folder is getting modified. 

`Correct typo`: I'm saying what exactly I did with LICENSE.md - I corrected a typo and that is exactly what I say. Seems straightforward right?

(also an interesting add-on: it's a good practice to say `Correct typo` instead of `Corrected typo` - think of it this way - you are instructing Git to do something so the language of your commits need to be in an instruction sort of manner - "Correct this typo, Git" and not "I have corrected this typo, Git")

That's it for this lesson! If you did it right, you should see your commit in the output of `git log`. 

In the next task, we will see how to "push" this commit!



