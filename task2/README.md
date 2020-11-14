# Task 2

Now, your commit is only visible to you i.e. it is your machine.

How do you "upload" it so that anyone can see, fork, clone and modify it themselves?

## Remote

Type `git remote -v`  in your terminal.

You should see something like:

`
origin https://github.com/< your username >/learn-git.git
`

Fancy words incoming!

### Origin and Upstream

Let's do a quick recap first.

The very first step you did on this tutorial, was to fork this repository.

What "fork" does is it creates a copy of the repository under your name.

Then you "clone"d your forked repository to your local machine.

Now when you did `git remote -v` it shows you from where you cloned *your* repository.

Remembering this is simple and important right now - and now whatever commits you "push" or "upload" are going to be the place where "origin" points to - which is your forked repository.

What's upstream? We will see about that later. Let's worry about "push"ing our commits first.

### Push

`git push`

That's it. You'll be prompted for your username and password, fill 'em out and you're done!

Within a few seconds, your commit should appear on your forked repository on github.com/< your username >/learn-git





