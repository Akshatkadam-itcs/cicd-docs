# Setting Up GitHub Actions

GitHub Actions is a powerful CI/CD tool that helps you to build, test, deploy your code right from your GitHub repository.


## Step 1: Create a Workflow Directory

Inside your project's root folder, create a new directory:

```bash
mkdir -p .github/workflows

This is where all your CI/CD pipeline .yml files will live.


## Step 2: Create your first workflow file

Inside your workflows folder creta a file named

ci.yml

This is your workflow file that will define what actions to take when certain events happen in your repo.


## Step 3: Add Basic Workflow Code

Here’s a simple workflow to get started:

name: CI Pipeline

on:
  push:
    branches: [ "master" ]
  pull_request:
    branches: [ "master" ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Set up Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test


This pipeline will run everytime you push to master or pull a request targeting the master.


## Step 4: Commit & Push the Workflow

Make sure you save all your changes in the code, and run the following command to push the code:

git add .github/workflows/ci.yml
git commit -m "Add CI pipeline using GitHub Actions"
git push origin master

GitHub will automatically pick up this workflow and start running it when the trigger conditions are met.