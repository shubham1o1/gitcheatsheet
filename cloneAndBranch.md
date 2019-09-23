## How to clone and pull in gitlab *[[source]](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html)*:

### Add your Git username and set your email:

It is important to configure your Git username and email address, since every Git commit will use this information to identify you as the author.

In your shell, type the following command to add your username:

``` git config --global user.name "YOUR_USERNAME" ```

Then verify that you have the correct username:

```git config --global user.name```

To set your email address, type the following command:

``` git config --global user.email "your_email_address@example.com" ```

To verify that you entered your email correctly, type:

``` git config --global user.email ```

You’ll need to do this only once, since you are using the --global option. It tells Git to always use this information for anything you do on that system. If you want to override this with a different username or email address for specific projects or repositories, you can run the command without the --global option when you’re in that project, and that will default to --local. You can read more on how Git manages configurations in the [Git Config](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration) documentation.

### Check your information

``` git config --global --list ```

---
### Basic Git commands

#### Initialize a local directory for Git version control

``` git init ```

This creates a .git directory that contains the Git configuration files.

Once the directory has been initialized, you can add a remote repository and send changes to GitLab.com. You will also need to create a new project in GitLab for your Git repository.

---

#### Clone a repository

To start working locally on an existing remote repository, clone it with the command 

```git clone <repository path>```

You can either clone it via HTTPS or SSH. If you chose to clone it via HTTPS, you’ll have to enter your credentials every time you pull and push. You can read more about credential storage in the Git Credentials documentation. With SSH, you enter your credentials only once.

You can find both paths (HTTPS and SSH) by navigating to your project’s landing page and clicking Clone. GitLab will prompt you with both paths, from which you can copy and paste in your command line.

As an example, consider this repository path:

**HTTPS:** ```https://gitlab.com/gitlab-org/gitlab.git```

**SSH:** ```git@gitlab.com:gitlab-org/gitlab.git```

To get started, open a terminal window in the directory you wish to clone the repository files into, and run one of the following commands.

---

#### Clone via HTTPS:

```git clone https://gitlab.com/gitlab-org/gitlab.git```

---

#### Clone via SSH:

```git clone git@gitlab.com:gitlab-org/gitlab.git```

---

Both commands will download a copy of the files in a folder named after the project’s name. You can then navigate to the directory and start working on it locally.

---

#### Switch to the master branch

You are always in a branch when working with Git. The main branch is the master branch, but you can use the same command to switch to a different branch by changing master to the branch name.

```git checkout master```

---

#### Create a branch

To create a new branch, to work from without affecting the master branch, type the following (spaces won’t be recognized in the branch name, so you will need to use a hyphen or underscore):

```git checkout -b <name-of-branch>```

---

#### Work on an existing branch

To switch to an existing branch, so you can work on it:

```git checkout <name-of-branch>```