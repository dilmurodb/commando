## GIT! (super useful to do this on the command line versus GUI)

00.	  `brew install git` (installs git, assumes you have homebrew)
01.   `git config --global user.name "Your Name"` (tells Git what your name is)
02.   `git config --global user.email "your_email@whatever.com"` (tells Git what your email is)
03.   `git init` (creates a repository of the current directory)
04.   `git add your-filename-here` (adds a new file)
05.   `git commit -m "First Commit"` (Commits file with a message in quotes)
06.   `git status` (tells you all about the git repositories' files).   git diff head (shows me whats different between whats getting committed and whats in there now)
07.   `git add` (stages changes to your repository BUT does not officially add them yet)
08.   `git add --all` (stages ALL changes to your repository, new in Git 2.0)
09.   `git reset HEAD filename-here` (undoes / unstages changes before they are committed). If you dont specify a comment, the system will drop you into Vim (text editor).  Hit ESCAPE key to change modes after inserting text...
10.   `git remote add local-repo-name-here git@github.com:your-name-here/repo-name-here.git` (basically this means you're connecting git to a remote git repository)
11.   `git remote add --mirror=push repo-name-here git@your.server.here:/your-repo-here.git` (establishes that your local is going to push to the remote)
12.   `git push local-repo-name-here master` (pushes my local up to github, 'local-repo-name-here MUST be the name of your repo')
13.   `git stash save` (will save changes that are not committed yet, like a faux branch)
14.   `git remote -v` (tells you what remote repos are connected to your local repo)
15.   `git config --global color.ui true` (sets up the cool command line color coding)
16.   `/home/your-name-here/.ssh/id_rsa.pub` (this is where you SSH keys live, youll have to hand the public side of your key to github)
17.   `git clone git://repo-url-goes-here.git destination-folder-here` (just put a space after the standard clone command to get a nice destination folder)
18.   `git clone -b branch-here remote-repo-here` (clone a remote branch)
19.   `git submodule add https://github.com/user-name-here/repo-name-here /destination/directory/here` (puts a git submodule into your current repo)
20.   `(FORCE FLAG example) git submodule add -f repo-here directory-here` (-f forces something to be added, even over the .gitignore file)
21.   `git status -s` (does a shorter version of the status thing)
22.   `git remote add origin https://github.com/user-name-here/repo-name-here`
23.   `git remote set-url -add origin https://github.com/user-name-here/repo-name-here` (specifically set's the URL for a remote repo, 'origin' in this case)
24.   `git push origin master` (pushes your code up to a remote, 'origin' is remote, 'master' is your local branch - must setup a remote beforehand)
25.   `git add -u` (adds deleted files into the commit)
26.   `git config core.autocrlf false` (fixes line ending errors)
27.   `git config core.safecrlf warn` (allows git to actually convery CRLF (win) to LF (linux/osx) line endings)
28.   `git config --global --add color.ui true` (turns git's coloring on)
29.   `git rm file-name-here.txt` (removes file | directory from the repo)
30.   `git ls-tree --full-tree -r HEAD` (list of all files in your repo)
31.   `git branch` (shows you a list of all branches; the one with a '*' is your current branch)
32.   `git tag -a v1.4 -m 'my version 1.4'` (tags your branch with a version)
33.   `git show v0.1` (git will show whats going on with a given tag)
34.   `git rm -r -f .sass-cache/` (recursively removes a whole bunch of junk from your repo)
35.   `git branch your-branch-here` (makes a new branch)
36.   `git checkout your-branch-here` (switches to doing commits against that branch)
37.   `git checkout -b your-name-here/your-topic-here` (establishes a new branch and switches to it so that future commits will be made against it)
38.   `git remote -v` (shows you all of your remotes)
39.   `git stash clear` (deletes everything off of stash)
40.   `git merge branch-name-here` (will merge branch-name-here with whatever branch you are on, do 'git pull' on your branch and make sure it's up to date with origin before merging!)
41.   `git reset --hard \[hash\]` (resets git to a given commit in the past on your branch)
42.   `git branch -v` (shows all branches, active one has '*' next to its name)
43.   `git log -n 5 --author=your-name-here` (shows the last 5 commits from a given author)
44.   `git reset` (undoes whatever you staged, all of it)
45.   `git push origin --delete your-branch-here` (deletes remote branches)
46.   `git branch -D your-branch-here` (deletes local branches, overrides conflicts)
47.   `git branch -d your-branch-here` (deleter local branches, will stop if uncommited changes are on branch)
48.   `echo .DS_Store > ~/.gitignore_global` (creates a global .gitignore_global file to store files you never want in your repo)
49.   `git config --global core.excludesfile ~/.gitignore_global` (will permanently ignore .DS_Store files in OSX)
50.   `git checkout --track origin/your-branch-here` (pulls in new remote branch to your local repo)
51.   `git remote rename old-repo-here new-repo-here` (renames your remote repo)
52.   `git stash apply` (puts uncommitted changes back onto current branch from stash)
53.   `git fetch` (pull all code off remote and puts it into a local cache, updates synced local branches)
54.   `git branch --track branch-name origin/branch-name` (if you don't have local branches synced with remotes, you can now sync them with this baby)
55.   `git submodule update --remote` (supposedly updates all submodules from .gitmodules, I have my doubts)
56.   `git add .`
57.   `git commit -m "Updated submodule"`
58.   `git push --follow-tags` (how to push tags to remote - they don't go with your code)
59.   `git fetch origin` (grabs all the stuff on your remote that isn't in your repo, puts it into a cache of sorts)
60.   `git checkout xyz` (creates tracking branch for whatever you fetched)
61.   `git branch --unset-upstream` (remove tracking branch's link to remote branch)
62.   `git rm --cached myfile.log` (removes file from repo cache, which is usually why you see .gitignore failures)
63.   `git rev-list --count branch-name-here` (shows you how many commits are in a given branch)
64.   `git push -f <remote> <branch>` (forces an overrite of remote with your branch, BE CAREFUL)
65.   `git rm -r --cached myFolder` (removes files from git repo but not filesystem - so they are there just not tracked. To me this implies that you should also be added whatever folder removed with this method into your .gitignore file).
66.   `git remote rename your-old-name-here your-new-name-here (rename remote)
67.   `curl -u 'USER' https://api.github.com/user/repos -d '{"name":"REPO"}'` (Using GitHub API v3 to create a repo from terminal without using web interface. Then 'git remote add')
68.   `git fetch <remote> <remote-branch>:<local-branch>` (creates a real local branch of a remote repo, not tracking branch)