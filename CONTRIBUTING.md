# Contributing a template

A template is a starting point, not a finished app: enough skeleton that the factory has something to build on, and enough intent that it builds the right thing. Open a pull request adding one top-level folder.

## Checklist

- [ ] **One folder**, named `<stack>-<app>` in lowercase (`go-shortener`, `django-recipes`).
- [ ] **`README.md`** with four sections: what the app is, what to install, how to build and run it, and how to start the factory (`ol start`). Link to [`docs/STARTING-AN-APP.md`](https://github.com/kigster/openlanes/blob/main/docs/STARTING-AN-APP.md) rather than restating its steps.
- [ ] **`.plans/APPLICATION.md`** from [`docs/application-template.md`](https://github.com/kigster/openlanes/blob/main/docs/application-template.md), all five headings filled. The non-goals must be real: they are what keeps the agents in scope.
- [ ] **A skeleton that builds** on a clean machine with only what the README says to install. Hello world is enough.
- [ ] **Two or three ⚪ seed plans** under `.plans/`, each with a `spec.md` that keeps the four headings, so `ol start` has work the moment it runs.
- [ ] **`.openlanes-template`** at the folder root, holding the minimum openlanes version, e.g. `min_version: 4.0.0`.
- [ ] **No `.openlanes.yml`.** `ol new` writes it when the template is copied.
- [ ] **A CI job** for the template that builds the skeleton.
- [ ] **A row** in the templates table in `README.md`.

## Upkeep

A template whose CI job fails across two openlanes releases moves to `unmaintained/`, out of the `ol new --example` list, until someone fixes it.
