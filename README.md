# ansible-scala

An Ansible role for installing Scala.

## Role Variables

- `scala_version` - Scala version
- `scala_sbt_version` - SBT version

## Testing
Tests are done using [molecule](http://molecule.readthedocs.io/). To run the test suite, install molecule and its dependencies and run ` molecule test` from the folder containing molecule.yml. To add additional tests, add a [testinfra](http://testinfra.readthedocs.org/) python script in the [tests](./tests/) directory, or add a function to [test_scala.py](./tests/test_scala.py). Information about available Testinfra modules is available [here](http://testinfra.readthedocs.io/en/latest/modules.html).

### Example 
```
# Download molecule, dependencies
$ pip install molecule

# Change to the top-level project directory, which contains molecule.yml
$ cd /path/to/ansible-scala

# Ensure that molecule.yml is present
$ ls
CHANGELOG.md                             molecule.yml
LICENSE                                  playbook.retry
README.md                                playbook.yml
ansible.cfg                              tasks
defaults                                 templates
handlers                                 tests
meta                                     

# We're in the right directory, so let's run tests!
$ molecule test

```