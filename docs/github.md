
The first thing you need to do, once only for every machine you use (such as wallace and/or your local computer), is to set up git by typing these lines at the terminal:

```bash
git config --global user.name "Joe Doe"
git config --global user.email "eamil@domain.com"
```

Now you have git configured in a way that you can access your repos (public and private), provided you have security permissions configured for that:

1. On wallace (or whatever machine you're trying to link with your github account):
    ```bash
    ssh-keygen -t ed25519 -C "email@domain.com"
    ```
2. Then go to GitHub, log in (if you're not already), click on your user icon in the upper right-hand corner, go to Settings, go to "SSH and GPG keys", and press the green "New SSH key" button.
3. Then, back on wallace, locate the public key that was generated in step 1 (`~/.ssa/id_ed25519.pub`) and copy the whole content and paste it into the "Key" box in GitHub.
4. Also in GitHub give the key a title, like "wallace", and then press "Add SSH key"
5. Then in wallace, clone the repository using repository's ssh link. Make sure that the directory `seal` doesn't already exist in your workspace.

    ```bash
    git clone git@github.com:washu-seal/seal.git
    ```


