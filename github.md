# How to use git!

This is an exercise to learn git. Git is basically Google Drive for developers and it's an essential skill for working together on a project.

This guide will assume you already have git installed. If you don't, you should follow the instructions for you operating system [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

This also assumes that you have made a github account and have been invited to the [GU-MAD organization](https://github.com/gu-app-club) on github.

- If you haven't made a github account yet, you can do so [here](https://github.com/).
- If _you have_ made a github account but haven't been added to the organization, ask one of the officers (Rudy or Evan) to add you!

# The rite of passage.

The goal of this rite of passage is to add your name to the `lets-learn-git` repository (repo).

A `repository` is a git word for a place where your files are stored. It's just a folder that lives somewhere else. (like dropbox)

### Cloning the repo

We're going to start by cloning the repository. In your terminal or your git command line, type this:

```
git clone https://github.com/gu-app-club/lets-learn-git.git
```

"Cloning" a repository will download a version of it to your computer. It will call the folder `lets-learn-git`. So let's go into that folder!

```
cd lets-learn-git/
```

### Signing your name!

If you `ls` right now, you'll see a `README.md` file. The `md` file type is Markdown, which is a super-simple language for writing documents. If you've ever done any formatting in Slack or on Reddit, it's very similar.

Every github has a `README.md` file that it shows as its main file. If you look at the repository [on github](https://github.com/gu-app-club/lets-learn-git), that's the text you see there.

Let's open up the README. You can open it up in any text editor. I like the text editor [atom](https://atom.io/), but you can use whatever you want. To open in `vim` for example, you would:

```
vim README.md
```

Inside the file, you should see a place where it says:

```
# Sign your name here!
```

Add your name to the list like so:

```
# Sign your name here!
- Grace Hopper
```

Then save the file.

### Creating a commit!

Once you're done, go back to your command line. We're going to upload our change to the repository!

We do this by creating a `commit`. A commit is a complete version of your code that you're adding. For example, every time your phone updates some app, behind the scenes, someone has pushed a commit (which might be called something like `Add cool feature XYZ; Fix death-bug`).

The important part: **A commit contains one or more file "changes".**

#### Time to check our status

Before we create our commit, we should check our `status`. A `git status` is git's way of telling you which files you've changed and therefore which files you could add to your commit. To see your status, in the command line:

```
git status
```

That should print out (in red) `modified` followed by the name of the file.

![example of git output](http://i.imgur.com/7ZZdp6N.png)

#### Adding files

Hopefully it should tell you that you've modified your `README.md` file. Now let's add that file to our commit.

```
git add README.md
```

If you call `git status` again, it should still say you've modified the file, but this time you will see it in green!

![example of git output when modified](http://i.imgur.com/qbZxgM0.png)

#### Committing

If we had other files, we would add them too. But we don't, so lets bundle everything into our commit. We can do this with:

```
git commit -m "I signed my name"
```

Notice the message after `-m`. You can put anything here, but it's typically expected for you to say something about what you did.

If you call `git status` now, you should see that git tells you:

```
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
nothing to commit, working directory clean
```

Notice that there are no longer any modified files. Git recognizes that the change's we've made are part of the commit that it has.

#### Pushing

We're almost done! We need to `push` our commit to the repo on github. Right now it only exists on our local computer. We can do this via:

```
git push
```

Git will ask you for your username password. **This is your github username and password**, not your computer's username and password.

If all goes well, you should see something like this:

```
Username for 'https://github.com': Flaque
Password for 'https://Flaque@github.com':
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 281 bytes | 0 bytes/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local objects.
To https://github.com/gu-app-club/lets-learn-git.git
   8e10b56..aa3f7b3  master -> master
```

# Hurrah!
![great success](http://s2.quickmeme.com/img/14/14c0f057abec6dabfc5be48cbbd0d904fef889a8781eee667984089207daf998.jpg)

If you go look at [the github](https://github.com/gu-app-club/lets-learn-git), you'll see your name on the list!

---

# TL;DR
How to push something in quick and easy steps.

1. (if you haven't already) clone the repo: `git clone <repo_url_here>`
2. Make changes.
3. `git add *`
4. `git commit -m "message here"`
5. `git push`
