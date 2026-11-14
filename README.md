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

## Verify

```bash
curl -s http://127.0.0.1:5000/
# Index Page

curl -s http://127.0.0.1:5000/hello
# Hello, World
```

Both strings come back with no framework machinery in between: two routes, two handlers, two lines of output. A `404` on either means the server started in a different directory — `flask run` discovers `app.py` from the working directory, not from the file you edited.

## Why this shape

One file, and no `requirements.txt`, because the first decision in a Flask project is how much structure to add, and a starter that answers it on the developer's behalf is a starter they spend an afternoon unwinding. `pip install Flask` is the whole dependency step; when a second package appears, `pip freeze > requirements.txt` takes one command and produces a file that matches the project rather than the template.

The development server is what `flask run` starts, and that is deliberate: this repository is for the first hour of a project, not for serving traffic. Moving to a WSGI server is a deployment decision with its own unit — [infra-blocks](https://github.com/kamaslau/infra-blocks) covers the part that comes after.

Two routes rather than one, because the second route is where a reader learns that adding a route is a decorator and a function, not a blueprint, a module and a registration call.

## Use this template

*Use this template* gives you a repository you own, with no history and no link back here — the right shape for
the first commit of a real app. Clone it instead when you want to follow changes to the starter itself;
a repository created from the template never receives them.

## License

MIT — see [LICENSE](./LICENSE). Take what is useful.

---

Built by [Kamas Lau](https://www.kamaslau.com/works?utm_source=github&utm_medium=repo-readme&utm_campaign=always-on&utm_content=starter) — I do this for foreign companies operating in China, on their own infrastructure.
