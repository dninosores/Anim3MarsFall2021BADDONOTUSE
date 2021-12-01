# Anim3Fall2021Mars

**Use unreal version 4.27.1**

To work with the unreal project, install github desktop from https://desktop.github.com/.

(Optional) You can get some fun extra features like icons in the unreal editor that tell you whether you have the most recent version of a file by opening the unreal project, right clicking any asset in the content browser, selecting "Connect to Source Control" in the right-click menu, and selecting "Git (beta)" as the provider in the popup (all of the other fields should be filled in automatically). More info about source control and unreal can be found here https://docs.unrealengine.com/4.27/en-US/Basics/SourceControl/

# How git works
Git is a version control application, which means that it automatically syncs the project across all of our devices so we don't have to worry about emailing files back and forth. It keeps track of a timeline of the project, with all of the changes that everyone has made to it. You can also branch off of that main timeline to work in your own personal version of the project and then merge your changes back into the main timeline, which means that you can make any change you want and not need to worry conflicting with other people's changes until you're finished making them.

## How to make changes to the project

### First-time setup
1. Install github desktop from https://desktop.github.com/ and open it. You don't need to enter in an administrator password to install github desktop, so you can do this on computers in the animation lab.
2. Sign in to your github account and enter in your name and email when prompted (this will be how your name shows up when you make changes to the project).
3. Click "Clone a repository from the internet". The repository is the main project folder.
4. Either find "dninosores/Anim3Fall2021Mars" in the list of repositories or go the the URL tab and enter "dninosores/Anim3Fall2021Mars" into the repository URL box.
5. Set "local path" to be the place where you want the project to be saved on your computer and press Clone. This will download the project to your computer.

### Making changes
1. In github desktop with the Anim3Fall2021Mars repository open, click on the "current branch" tab at the top of the screen. This will give you a list of all of the branches that currently exist in the project.
2. Click on the main branch to switch to it. The main branch is the currently most stable and up-to-date version of the project.
3. Click on the Fetch Origin button to check if anyone else has made changes to the main branch, and then if prompted, click on pull changes to download the new changes. You now have the most up-to-date version of the main branch on your computer.

**You generally don't want to make changes directly to the main branch because if you make a mistake or mess up someone else's work, that will become the most up-to-date version of the project and it will introduce those problems for everyone else. Instead, you can make your own personal copy of the main branch, make any changes you want without worrying about interfering with other people's work, and then once you're completely sure your changes are finished, add them all to the main branch at once. That's why we're going to be making a new branch in the next steps.**

4. Click on the "current branch" button again, but this time click on "new branch" to create a new branch. **Make sure you switch to the main branch and fetch origin/pull before making the your new branch to make sure that everything is up-to-date.** Call the branch "yourname-name-of-the-thing-you're-working-on". For example, if I'm making a branch where I plan to block out the engine room, I would call the branch olly-engine-room-blockout. For the "create branch based on..." section, select "main" to branch off of the main branch, then click "create branch".
5. When you create a new branch, git will make the branch on your local computer but won't automatically upload it to the internet. In order to upload your branch so that other people can see it, press the "Publish branch" button that should appear after you create a new branch.

**Now you're working in your own branch. You can make any changes you want and it won't affect anyone else."

6. Open the project in unreal and make some changes to it.
7. When you make changes, you'll see the files you've changed pop up in github desktop.
8. In order to save your changes to git, you need to make a commit. A commit is a group of changes that you save to a branch. If you think of your branch as a timeline of all the changes you've made to the project, a commit is a single point on the timeline. To commit your changes, go to github desktop, type a summary of the changes that you've made, and press the blue "commit" button. This will save your changes to your local computer.
9. In order to make it so that other people on other computers can access your changes, you need to push those changes to the internet. You can do this by clicking the "push origin" button.

**You generally want to make a commit every time you reach some sort of milestone with your progress. Think of it sort of like incrementally saving a Maya project--at any time if you mess something up, you can roll back to a previous commit and work from there, so committing early and committing often is a good rule of thumb.**

**As other people work on the same project, they will eventually end up merging their changes into the main branch. However, since your're working on a copy of the main branch, you won't be able to see these changes until you merge them in yourself. To do this, click the "current branch" button, select your branch, click "choose a branch to merge into..." at the bottom of the screen, select the main branch, and click "create a merge commit". This will update your copy of the main branch to look like the most up-to-date version of the main branch without you losing any of your changes.**

**When you merge branches together you might end up with a MERGE CONFLICT. This happens when you changed a file on your copy of the main branch, and someone else also changed that file on the main branch, and git doesn't know which version of the file to use when combining those branches together. Github will usually ask you whether you want to keep your version of the file or the version of the file that was saved to the main branch. You should check with whoever worked on that file last if you choose to keep your version of it since choosing your version will delete theirs. You can avoid merge conflicts by merging the main branch into your branch often.**

10. Once you finish making changes on your branch, you have to make sure that merging them in to the main branch won't break the game. Do ths by merging the main branch into your branch using the steps in bold above, then running the game to make sure that it works. If you find any problems, fix and commit them, then merge main again. Keep doing this until merging main doesn't create any issues.
11. Now you can be pretty sure that merging your changes into the main branch won't cause problems for anyone else. To finalize your changes and merge them into the main branch, click on the "Create Pull Request" button in github desktop. A pull request is a request to get your changes merged into the main branch. You should give it a name and description that describe the changes that you've made on your branch. Other people can look at your pull request and leave feedback on it before it is officially merged into the main branch.
12. On the pull requests's page on github.com, click the "Merge Pull Request" button to merge it into master, and then press the "delete branch" button to delete the copy of the main branch that you were working on. 

Congrats! Your changes are now officially saved to the project!


## Git Words
 - **Repository**: The main project folder.
 - **Clone**: Cloning a repository is when you download it to your computer for the first time.
 - **Remote**: Stuff that's stored on the internet so everyone can access it (when people talk about the "remote repository", they mean the version of the project that's stored online)
 - **Origin**: The one true version of the project that everything is a copy of. In this case, origin is the version of the project that is saved online at github.com (as opposed to the version of the project that you have saved to your computer)
 - **Local**: Stuff that's stored on your computer so that only you can access it
 - **Branch**: A branch is a timeline that keeps track of changes that have been made to a project.
 - **Main**: "Main" is the name of the project's main branch. It contains the complete history of the entire project, as well as the most up-to-date version of it. You generally don't want to make changes directly to the main branch--instead, you should make a personal branch that forks off of the main branch, make your changes there, and then merge those changes into the main branch once you're sure they work. This keeps bugs and mistakes from being added to the main branch.
 - **Commit**: A commit is a group of changes that have been saved to a branch. When you make changes to a project, they don't get saved to git until you commit them.
 - **Push**: When you commit changes to git, they get saved to your computer but don't get uploaded to the cloud. This means that other people on other computers can't access them. In order for your changes to be available to other people, you have to push them to the remote repository.
 - **Pull**: Downloads the newest version of a branch to your computer
 - **Fetch**: Check for changes that other people have made to the project and pushed to github
 - **Merge**: Taking the changes from one branch and adding them to another. This usually happens when you finish making changes on your personal branch and want to add them to the main branch.
 - **Pull Request**: A request to merge one branch into another branch. The idea is that you can get feedback on your personal branch before you merge it into the main branch.
 - **Merge Conflict**: When two people make changes to the same file at the same time on different branches and git doesn't know which version of the file to use when they're getting merged together. Github Desktop will ask you to resolve the conflict by picking which version of the file you want it to take.
