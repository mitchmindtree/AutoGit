AutoGit
=======

A small python script for automating the Git process. Using it
alongside the vimscript in Vim allows you to just type:

    :AutoGit <message>

And this will do the following:
- `git add -A`
- `git commit -m '<message>'`
- `git push origin master`
- If github requests user & pw, AutoGit will kill the process
and instead begin configuring your repo so it never has to
ask for your user & pw again. i.e.
    - Find repo name
    - Request `<USER>`
    - Request `<PW>`
    `git config remote.origin.url https://<USER>:<PW>@github.com/<USER>/<REPO_NAME>`

You can also call the python script by itself if you prefer:

    $ python AutoGit.py <path> <message>

Dependencies
------------

- Docopt for the CLI.
- pexpect for working with Git CLI.

ToDo
----

- Thread the whole process, only be visible if needed for user/pw.
- If tmux session, have it occur in separate tmux window.
- If no tmux session, have it occur in separate tab.

Note
----

I'm not sure if it'll work on Windows, but it should work
on Mac / Linux.


by Mitchell Nordine
