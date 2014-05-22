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
    - `git config remote.origin.url https://<USER>:<PW>@github.com/<USER>/<REPO_NAME>`

You can also call the python script by itself if you prefer:

    $ python AutoGit.py <path> <message>


Dependencies
------------

- [Docopt] (http://docopt.org/) for the CLI.

    $ pip install docopt

- [pexpect] (http://pexpect.readthedocs.org/en/latest/) for working with Git CLI.

    $ pip install pexpect


Note
----

I'm not sure if it'll work on Windows, but it should work
on Mac / Linux.


by Mitchell Nordine
