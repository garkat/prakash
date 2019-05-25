# Git

## Initial set up

- Run `git config --list` in the git repo you're working on. If you haven't set up global user name, email, and if you're working on the current repo for the first time, then user name/email will be missing. However, they can be set by running the following commands:

- Run `git config user.name YOUR_USER_NAME`

- Run `git config user.email YOUR_EMAIL_ADDRESS#`

Side note: You can use an anonymous email address while working on an open source project. Click below to check your GitHub email settings.

[GitHub email settings](https://github.com/settings/emails)

## Forking a project

- First of all, fork the repo that you want to contribute to. For instance, if you want to contribute to this repository, then go to <https://github.com/aukha-saukha/prakash>, and click on the fork button.

![How to fork a repo](img/how-to-fork-a-repo.png 'How to fork a repo')

- Now, please go to your forked repo page. It should be something like `https://github.com/YOUR_USER_NAME/YOUR_FORK_OF_ORIGINAL_REPOSITORY`.

- Click on the "Clone or download" button to get the URL that can be used to clone the repo.

**Step 1:**

![How to get fork repo URL: step 1](img/how-to-get-fork-repo-url-1.png 'How to get fork repo URL: step 1')

**Step 2:**

![How to get fork repo URL: step 2](img/how-to-get-fork-repo-url-2.png 'How to get fork repo URL: step 2')

- Please go to your computer's terminal, and run `git clone https://github.com/YOUR_USER_NAME/YOUR_FORK_OF_ORIGINAL_REPOSITORY.git`. It's the same URL that you got in the previous step.

- The remote repo need to be configured so that it points to the correct upstream repo. It can be done by running `git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git`.

![How to get upstream repo URL](img/how-to-get-upstream-repo-url.png 'How to get upstream repo URL')

- You can verify that the upstream repo has been set correctly by running `git remote -v`. The output should look like below:

  ```bash
  origin    https://github.com/YOUR_USER_NAME/YOUR_FORK_OF_ORIGINAL_REPOSITORY.git (fetch)
  origin    https://github.com/YOUR_USER_NAME/YOUR_FORK_OF_ORIGINAL_REPOSITORY.git (push)
  upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
  upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)
  ```

- You can sync your forked branch by running `git fetch upstream`, followed by `git merge upstream/master`.

## Creating a new branch for development

- Run `git checkout -b BRANCH_NAME`.

- Make required changes.

- Run `git status` to list all the files that have changed.

- Run `git diff FILE_NAME` to make sure the files have only the changes that you're expecting. You can also use your favorite IDE to see `git diff`.

- Run `git add ALL_RELEVANT_FILES`

- Run `git commit -m 'COMMIT_MESSAGE_THAT_EXPLAINS_WHAT_COMMIT_IS_ABOUT'`

- Push your branch to the remote repository by running `git push -u origin BRANCH_NAME`.

## Raise a pull request (PR)

Once a developer is done with the required update, and the code has been committed, then a PR should be raised. Click below to learn about how to raise a pull request.

[Creating a pull request](https://help.github.com/en/articles/creating-a-pull-request)

## Merging into master branch

Once a PR has been approved and it doesn't have any merge conflicts, then it can be merged into the master branch. Once the code has been merged, the updated code is available to all other develoepers too.
