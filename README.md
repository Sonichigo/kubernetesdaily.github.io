# KubeDaily Website 


## Running the site locally

To run the website locally, you need to have the [Hugo](https://gohugo.io) static site generator installed (installation instructions [here](https://gohugo.io/getting-started/installing/)). Once Hugo is installed:

```bash
yarn install
hugo server --buildDrafts --buildFuture
```

This starts Hugo in local mode. You can see access the site at http://localhost:1313.



## New versions of the docs

To create a new version of the documentation:

1. Copy the most recent version of the documentation to create a new version. If the most recent version is 1.2.4 and you'd like to create 1.2.5:

    ```sh
    cp -rf content/docs/1.2.4 content/docs/1.2.5
    ```

1. Add the version to the `params.versions` list in [`config.toml`](./config.toml). Make sure that the list has the latest versions first.

## Contributing to docs

### Sign Off on All Commits

All contributions to the docs need to be signed off.

To sign off when creating a commit, run:

    git commit -m "Commit message" -s

To sign off when editing the docs with the GitHub UI, enter a name for your commit, then in the large field below the commit message, enter the signoff text with your own name and email, e.g.:

    Signed-off-by: name  <email>

To sign off on a commit that is already in a pull request, 

1. Head to your local branch and run:

    `git commit --amend -s`

    Now your commits will have your signoff. 
    
2. Next run:

    `git push --force-with-lease origin patch-1`

    In this example, `patch-1` is a local branch.


### Documenting Upcoming Features

The documentation is split into multiple versions, with a directory for docs corresponding to each Longhorn version. For example, Longhorn 0.8.0 docs are in `content/docs/0.8.0`.

To make changes to the docs that are specific to an upcoming release, use the specific version branch, e.g. `v1.1.1` which contains the directory `content/docs/1.1.1` for that version.
