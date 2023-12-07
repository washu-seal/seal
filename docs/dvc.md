Please see [dvc documentations](https://dvc.org/doc/command-reference) for more dvc commands and descriptions

**Some useful commands**
- `dvc add file`
- `dvc push -r remote file`
- `dvc pull -r remote file`
- `dvc repro dvc.yaml`

## General tips
- Each dataset has a dvc remote in wallace that you have to have an access in order to pull the data 
    - ask one of the senior persons in the lab to give you access for any project that you need to work on.

- Each project has 2 dvc remotes: `main` and `temp`; DO NOT push anything to `main` remote of a project unless everyone in that project is gonna need that for the whole lifetime of project (you can use `temp` instead ).