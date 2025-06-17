## Customiztion based on your tech stack

Setting up CI/CD pipeline isn't the only thing that is one-size-fits-all. It should fit perfectly based upon your unique tech stack you're using.

## For React Projects

Here’s a basic example for React apps using npm:

```yaml
name: React CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Code
        uses: actions/checkout@v3

      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'

      - name: Install Dependencies
        run: npm install

      - name: Run Tests
        run: npm test

      - name: Build React App
        run: npm run build


## For Node.js Projects

name: Node.js CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3

      - name: Use Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'

      - run: npm install
      - run: npm test


## For Python Projects

name: Python CI

on: [push]

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3

      - name: Set up Python
        uses: actions/setup-python@v5
        with:
          python-version: '3.10'

      - name: Install dependencies
        run: |
          python -m pip install --upgrade pip
          pip install -r requirements.txt

      - name: Run Tests
        run: pytest



## Best practices

- Use cache steps to speed up builds.
- Keep secrets in GitHub Secrets, not in .yml.
- Use matrix builds to test on multiple environments (Node versions, OS, etc.).

