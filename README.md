# empirical-zec

## First steps

This assumes that you are developing with `conda` and `python` 3.7+. These instructions should work for Windows when using Anaconda Prompt and for MacOS in Terminal (and by extension, likely will work on Linux).

1. Create your environment:

```
conda env create -f environment.yml
```
2. Make nice version-control friendly notebooks, which will remove all output and data upon committing. Run
```
nbstripout --install
```

3. Examine .gitignore and decide where you want to put any large input or output datasets that you don't want to commit to GitHub, and fill in these paths.

## Operation 

### Developing your package

Most of the time your workflow will look like this

```
conda activate empirical-zec
jupyter notebook
```

### Updating requirements

As you build the package you will likely want to add more dependencies. Edit the `environment.yml` file and run
```
conda env update -f environment.yml --prune
```

Please do not overwrite the `environment.yml` file using `conda env export`, as this exports everything in your local environment including all sub-dependencies and OS-specific packages (and sometimes local paths).
