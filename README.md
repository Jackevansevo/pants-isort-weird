Demostrates difference in behaviour invoking isort directly vs via pants

I'm using the following isort configuration in `pyproject.toml`

    [tool.isort]
    profile = "black"


Run this first (to install isort locally in a virtualenv)

    pants export ::


Running

    dist/export/python/virtualenvs/tools/isort/bin/isort main.py

Then

    pants fmt --only=isort main.py


Results in differnet formatting with tools appearing to disagree.
