
# Requirements

This is a directory of requirements files. They are maintained using `pip-tools`: 

* `*.in` - for developers to enter required packages 
* `*.txt` - autogenerated by `pip-tools` hash-lock the specific versions for production

## Upgrading

When you want to upgrade (be sure to run from main treeherder directory, this this directory)

    pip-compile --upgrade --generate-hashes --output-file requirements/common.txt requirements/common.in
    pip-compile --upgrade --generate-hashes --output-file requirements/dev.txt requirements/dev.in
    pip-compile --upgrade --generate-hashes --output-file requirements/docs.txt requirements/docs.in

> [see pip-tools for more information](https://pypi.org/project/pip-tools/)