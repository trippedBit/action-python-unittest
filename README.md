# python-actions
Action execute Python unittests.
<br><br>
## License
Please see [LICENSE](LICENSE)
<br><br>
## Usage
Create a workflow file inside your repo in .github/workflow and add the following.
Change the name and the triggering event to fit your needs.
```yml
name: unittests

on: [workflow_dispatch]

jobs:
    translation_job:
      runs-on: windows-latest
      name: Unittest execution
      steps:
        - uses: trippedBit/action-python-unittest@v1.0.0
          with:
            files: tests/test_mymodule.py tests/test_unit.py
            python-version: 3.9.6
```
### Inputs
The following inputs are available:
* files: List of test files. This is a required input.
* python-version: Python version to use. This is a required input.