Reproduce detect-secrets [issue 192][1]

Create venv and execute

    $ make .venv
    $ source .venv/bin/activate

Baseline was created by:

    $ detect-secrets scan docker-compose-base.yaml > .secrets.baseline


[1]: https://github.com/Yelp/detect-secrets/issues/192
