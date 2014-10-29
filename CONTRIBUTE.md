#Contributing to the project

We would love for you to contribute to our source code and to make the project even better than it is!

 - [My branch Workflow](#workflow)
 - [Question or Problem?](#question)
 - [Issues and Bugs](#issue)
 - [Submission Guidelines](#submit)
 - [Commit Guidelines](#commit)
 - [Further Info](#info)

## <a name="workflow"></a> Our Branch Workflow

* Master - This our stable or "Release" branch, this is the code that gets pushed into production

Think of our branches this way: 
* Master=Stable

## <a name="question"></a> Got a Question or Problem?

Most questions can be answered by reading the [README]((https://github.com/caseyrichins/gentoo_mass_deploy/blob/master/README.md) or CONTRIBUTING md files. If you have a question that is not answered here
please refer to [Further Info](#info) at the bottom of this document.

## <a name="issue"></a> Found an Issue?
If you find a bug in the source code or a mistake in the documentation, you can help us by
submitting an issue to our [GitHub Repository][github]. Even better you can submit a Pull Request
with a fix.

### Security vulnerability disclosure

Please report suspected security vulnerabilities in private by creating a New Issue request and label it ```Security```.

## <a name="submit"></a> Submission Guidelines

### Submitting an Issue
Before you submit your issue search the archive, maybe your question was already answered.

If your issue appears to be a bug, and has not been reported, open a new issue. 
Help us to maximize the effort we can spend fixing issues and adding new features, by not reporting duplicate issues.

* **Related Issues** - has a similar issue been reported before?
* **Suggest a Fix** - if you are not able to fix the bug yourself, perhaps you can point to what might be
  causing the problem (line of code or commit)

### <a name="pull"></a>Submitting a Pull Request
Before you submit your pull request consider the following guidelines:

* Search [GitHub](https://github.com/caseyrichins/gentoo_mass_deploy/pulls) for an open or closed Pull Request
  that relates to your submission. You do not want to duplicate current issues.
* Make your changes in a new git branch

     ```shell
     git checkout -b my-fix-branch master
     ```
* Commit your changes using a descriptive commit message that follows our
guidelines and sign your commit with you GnuPG(gpg) Key.

     ```shell
     git commit -a -S -m 'Commit Message'
     ```
  Note: the optional commit `-a` command line option will automatically "add" and "rm" edited files.

  Note: the optional commit `-S` command line option is needed for you to Sign your commits with your Key.

* Push your branch to GitHub:

    ```shell
    git push origin my-fix-branch
    ```
* In GitHub, send a pull request to `gentoo_mass_deploy:master` to be included in the next release cycle 

* If we suggest changes then
  * Make the required updates.
  * Rebase your branch and force push to your GitHub repository (this will update your Pull Request):

    ```shell
    git rebase master -i
    git push -f
    ```

#### After your pull request is merged

After your pull request is merged, you can safely delete your branch and pull the changes
from the main (upstream) repository:

* Delete the remote branch on GitHub either through the GitHub web UI or your local shell as follows:

    ```shell
    git push origin --delete my-fix-branch
    ```

* Check out the master branch:

    ```shell
    git checkout master -f
    ```

* Delete the local branch:

    ```shell
    git branch -D my-fix-branch
    ```

* Update your master with the latest upstream version:

    ```shell
    git pull --ff upstream master
    ```


## <a name="commit"></a> Git Commit Guidelines

### Fork

Fork the project [on GitHub](https://github.com/caseyrichins/gentoo_mass_deploy) and check
out your copy.

```
$ git clone git@github.com:username/gentoo_mass_deploy.git
$ cd gentoo_mass_deploy
$ git remote add upstream git://github.com/caseyrichins/gentoo_mass_deploy.git
```

In case of doubt, open an issue in the [issue tracker](https://github.com/caseyrichins/gentoo_mass_deploy/issues)

Especially do so if you plan to work on something big.  Nothing is more
frustrating than seeing your hard work go to waste because your vision
does not align with that of a project maintainer.


### Configure Git

Make sure git knows your name, email address and key:

```
$ git config --global user.name "J. Random User"
$ git config --global user.email "j.random.user@example.com"
$ git config --global user.signingkey gpg-key-id
```
### Sign your Commit
I *Encourage* you to sign your commit using your GnuPG(gpg) key. Refer to [GnuPG](http://www.gnupg.org) for more information.

See [Submitting a Pull Request](#pull) for instruction on signing commits.

  Note: the optional commit `-S` command line option is needed for you to Sign your commits with your Key.

## <a name="info"></a> Further Information
You can find out more detailed information about contributing by contacting [Casey Richins](https://github.com/caseyrichins)

### Keeping your fork in sync
Visit [Github Help](https://help.github.com/articles/syncing-a-fork/) for a Howto on keeping your fork in sync.
