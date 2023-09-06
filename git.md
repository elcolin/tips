# git
Tips and use of git.

## Remote

Two Repositories: **team** and **personal**
I wish to synchronize my personal git with my branch on my team project.
A branch needs to be created in our team repo:

    git branch ecolin
The "ecolin" branch will be created.
Get into the personal repo and add a remote:

    git remote add team https://github.com/elcolin/team

Then it's important to pull from the wanted branch:

    git pull team ecolin

**To add permanantly**

    git config --global --add remote.team.url https://github.com/url/to/team/repo

**NOT MANDATORY**
Does not work if there is a name mismatch
Then you can create a tracking relationship between your main branch on your personal repo and your branch on the team repo:

    git branch --set-upstream-to=team/ecolin main

You won't have to specify the remote each time you push.

To push on your team repo and branch:

    git push team HEAD:ecolin

To push on your base repo:

    git push origin