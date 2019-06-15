Reproduce detect-secrets [issue 192][1]

Create venv and execute

    $ make .venv
    $ source .venv/bin/activate

Baseline was created on the master branch by:

    $ detect-secrets scan docker-compose-base.yaml > .secrets.baseline

Checkout develop branch which contains a password not in baseline

    $ git co develop

Run the hook:

    $ detect-secrets-hook --baseline .secrets.baseline

[1]: https://github.com/Yelp/detect-secrets/issues/192
