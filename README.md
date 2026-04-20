# The Missing Semester of Your Machine Learning Education

Classes and online courses teach you ML theory and how to train different kinds of models, but there's a whole set of practical skills that are rarely covered: exploratory data analysis, ML system design, ML ops, and more. This website aims to fill that gap, modeled after [MIT's Missing Semester](https://missing.csail.mit.edu/).

**Live site:** <https://georgerpu.github.io/missing-semester-ml/>

## Building the website

```bash
uv sync
uv run jupyter-book start
```

## Adding content

1. Create a `.md` or `.ipynb` file under `modules/`.
2. Register it in the `project.toc` list in `myst.yml`.
3. Run a local build to verify.

## License

[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
