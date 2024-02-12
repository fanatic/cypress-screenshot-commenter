# cypress-screenshot-commenter

This action compares cypress/screenshots on the current branch with its head branch
and comments on the PR with the differences.

1. Fetch screenshot artifact and save them on the cypress-screenshots branch.
2. Run odiff to compare folders and generate a diff.
3. Comment on the PR with a table with the existing, new, and difference screenshots.

# Local testing

1. `act push  --artifact-server-path artifacts`
2. `act -j compare-screenshot-test   --artifact-server-path artifacts -P ubuntu-latest=ghcr.io/catthehacker/ubuntu:full-latest`
