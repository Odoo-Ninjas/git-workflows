# Setup Robotests/Unittests for odoo projects

*  create .github/workflows/testing.yml

```yaml

name: testing
on:
  push:
    branches-ignore:

permissions: write-all

jobs:
  run_robo_tests:
    uses: Odoo-Ninjas/git-workflows/.github/workflows/robotests.yml@v9
    with:
      enabled: true
      projectname: myproject

  run_unit_tests:
    uses: Odoo-Ninjas/git-workflows/.github/workflows/unittests.yml@v9
    with:
      enabled: true
      projectname: myproject

```