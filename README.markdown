Gist: The Script
================

Works great with Gist: The Website.

Installation
------------

    curl http://github.com/defunkt/gist/raw/master/gist.rb > gist &&
    chmod 755 gist &&
    sudo mv gist /usr/local/bin/gist

Use
---

    gist < file.txt
    echo secret | gist --private # or -p
    gist 1234 > something.txt


Authentication
--------------

Just have your git config set up with your GitHub username and token.

    git config --global github.user "your-github-username"
    git config --global github.token "your-github-token"

You can find your token under [your account](https://github.com/account).

You can also define github.token to be a command which returns the actual token on stdout by setting the variable to a command string prefixed with `!`. For example, the following command fetches the token from a password item named "github.token" on the Mac OS Keychain:

    token = !security 2>&1 >/dev/null find-generic-password -gs github.token | ruby -e 'print $1 if STDIN.gets =~ /^password: \\\"(.*)\\\"$/'


Ninja vs Shark
--------------

![Ninja vs Shark](http://github.com/defunkt/gist/tree/master%2Fbattle.png?raw=true)
