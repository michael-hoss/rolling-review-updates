# GitHub permissions for the workflow

Here is how to give the `actions/checkout@v3` its needed permissions to your repo(s), especially for checking out also submodules.

## Create a personal access token (PAT)

In GitHub's **(Account) Settings** -> **Developer Settings**, create a PAT an copy its contents to the clipboard.

### Recommended: create a *fine-grained* PAT
- give it *read-only* permissions for *Contents* and *Metadata* on your main repo **and** its submodules
- name it `CHECKOUT_FOR_{MAIN_REPO_NAME}` (name is only for recognizing it later on)

### Alternative: create a *classic* PAT 

A non-fine-grained (classic) PAT has equal permissions on all of your repos.
- allow only the scope "workflow"
- somewhat less secure -> better only use this in entirely private repos 


## Create a repo secret 

In **(Repo) Settings** -> **Secrets and variables** -> **Actions**
  - name it `MY_REPO_PAT` (or however the workflow `yml` file refers to it) 
  - paste the previously copied PAT secret as contents
  
## Further notes
- repeat this process whenever the PAT expires (validity of fine-grained PATs is limited to one year)
