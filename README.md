Vale Specification Experiment
=============================

This repository has a specification for Tempe Value.
Details in vale-spec/docs/index.md.

This is an experiment in specification writing that includes position
paper elements on architecture instead of just describing what
implementors need to know to implement the spec.

The goal is twofold:

- Define a specification for something useful.
- Help non-professional spec writers produce software specifications
  using AI by providing a spec that has elements that can be reused in
  other specifications.

This specificaiton has sections on, for example, ensuring that access
control checks reliably happen.  This specification goes into more
detail than usual on *why* and *how*, not just *what*, hence the
position paper-y feel of the spec.  Since it does, hopefully people
who are not steeped in systems architecture can more effectively adapt
and reuse elements of this specification in their own work whether
vibey or not.

----

All commits to this repository are either human authored or AI
authored, never both, and the commit messages identify them as such.

----

This specification is rendered using `mkdocs`.  The poetry configuration
allows running mkdocs easily.

From the directory containing this README:

```sh
poetry run bash -c "cd vale-spec && mkdocs serve"
```


## Decidious Synchronization

When pulling the repo and a new `deciduous.db` exists:

```
cp .deciduous/decidious.db .deciduous/deciduous_mine.db
git checkout origin/their-branch .deciduous/deciduous.db
claude
"Run through the two deciduous databases in .deciduous and merge them, especially considering trees that touch the same work"
```
