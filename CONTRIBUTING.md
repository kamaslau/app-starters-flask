# Contributing

This repository is one starter of the app-starters family: Python on [Flask](https://flask.palletsprojects.com/), two routes and a development server.

Default port: 5000, Flask's own default. `flask run --port 3000` moves it, and nothing here hardcodes it.

## The shape a change has to keep

A starter, not a framework: readable in a minute, one file, no dependency that is not Flask itself. The point of this repository is the first commit of a real project, and a project that starts with a build system has already made a decision it cannot explain.

The test for any change: could someone who has never seen this repository have both routes answering from the README alone?

## Pull requests

- **`app.py` stays one file** until it is replaced. When a change needs a package layout, that change belongs in the project built from this starter, not here.
- **No `requirements.txt`, no lockfile.** The only dependency is Flask, and a lockfile you did not generate is worse than one command you typed. If a second dependency ever becomes necessary, that is the moment to add one — with the lockfile.
- **The README is English.** Chinese belongs only under a *Notes for deployments in China* section, when there is something true to write there.
- **`Verify` has to keep proving something.** Any change in behaviour updates the command in that section.
- **Commits**: imperative subject, one concern per commit. `fix: name the port in the run command` is the shape. `update` is not.

## Adding a starter

Open an issue on [infra-blocks](https://github.com/kamaslau/infra-blocks) before writing anything — the family is meant to stay small, and two starters for the same framework is a maintenance cost rather than a choice.

If it is accepted:

1. Repository named `app-starters-<framework>`, MIT license, description in the form *what it is + what it gives you*.
2. README with the sections used across the family: title and one-line purpose, Run, What it gives you, Verify, Why this shape, Use this template.
3. `is_template` enabled, and a row in the index under *Not in this list*.

## Reporting a problem

Open an issue with four things: the command you ran, what you expected, what happened, and the output of `flask run`. Without the last one, most reports turn into guesswork.

---

Part of the app-starters family · MIT
