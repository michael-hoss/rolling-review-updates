# GitHub permissions for the workflow

Here is how to give the `actions/checkout@v3` its needed permissions to your repo(s).

## Create a personal access token (PAT)

In GitHub's **(Account) Settings** -> **Developer Settings**

### Create a *fine-grained* PAT
- give it only *read* permissions for *Actions* on only the needed repos (main repo *and* your submodules)
- name it `CHECKOUT_FOR_{MAIN_REPO_NAME}`
- copy its contents (the secret) to the clipboard

### Alternative: create a classic PAT 

A non-fine-grained (classic) PAT has equal permissions on all of your repos (probably a bit less secure).
- allow only the scope "workflow"
- copy its contents (the secret) to the clipboard

## Create a repo secret 

In **(Repo) Settings** -> **Secrets and variables** -> **Actions**
  - name it `MY_REPO_PAT` (this variable is used by the `create_latex_pdf_release.yml`) 
  - paste the previously copied PAT secret as contents
  
## Further notes
- now, the `create_latex_pdf_release.yml` workflow should work 
- repeat this process whenever the PAT expires (validity seems to be limited to one year)

