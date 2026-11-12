# app-starters-flask

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
![Repository size](https://img.shields.io/github/repo-size/kamaslau/app-starters-flask?color=56BEB8)

Python app starter with [Flask](https://flask.palletsprojects.com/): two routes and a dev server, small enough to read in a minute.

## Run

```bash
python3 -m venv venv
. venv/bin/activate
pip install Flask
flask run
```

`app.py` is the entry point. If you rename it, export the module name first — `export FLASK_APP=main`.

## What it gives you

- `/` → `Index Page`
- `/hello` → `Hello, World`

Two routes, not a framework tour. Replace them; that is the point of a starter.

There is no `requirements.txt` on purpose — the only dependency is Flask, and a lockfile you did not generate
is worse than one command you typed.

## Use this template

*Use this template* gives you a repository you own, with no history and no link back here — the right shape for
the first commit of a real app. Clone it instead when you want to follow changes to the starter itself;
a repository created from the template never receives them.

## License

MIT — see [LICENSE](./LICENSE). Take what is useful.
