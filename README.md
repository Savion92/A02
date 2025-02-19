# A02
#### A repository for IS117

## Git

The first step in using Git is to make sure your machine has Git installed and ready for use.
1. Check for installation by using the ```git``` command in your terminal.
   * If Git is properly installed you should see the following information on how to use Git.
   ![Screenshot from my machine](https://github.com/user-attachments/assets/d8da964b-46d4-47d8-9a20-3189b246f73c)
   * If Git isn't installed on your machine, you may be able to install git by running the command ```sudo apt-get install git-all``` on a Linux machine. More detailed instructions on installing Git can be found on Github. [Git installation guide](https://github.com/git-guides/install-git)
2. After installing git, it is important to configure Git using the command ```git config``` at the command line.
   1. Set your username by using the command ```git config --global user.name "yourUserName"``` 
   2. Set your email by using the command ```git config --global user.email "yourEmail@email.com"```
3. Using Git in a folder begins with initializing a Git repository.
   1. The first step is to have a folder created for your new project. For now we'll call this ```myProjectFolder```
   2. You'll need to make sure your in your project folder in your terminal. Use ```pwd``` to print the working directory
        ![Screenshot from my machin](https://github.com/user-attachments/assets/c8d42a3a-69ad-45a5-afa3-ee093e361367)
      * Use ```cd``` to change directories and reach your folder. If you're following along, the flow may look like this
        ![Screenshot 2025-02-19 at 9 32 43 AM](https://github.com/user-attachments/assets/aeb553fb-0af9-45fa-972f-0d8f289ed116)
   3. Once you've confirmed that you're in the correct folder initialize a git repository for that folder using the command
      ```git init```
      ![Screenshot 2025-02-19 at 9 36 09 AM](https://github.com/user-attachments/assets/e1fa0dd9-852a-4667-a2b3-07a82b7506ec)
  4. Adding files to staging prepares them to be commited to your repository, it is an important step in tracking your changes. When adding files to staging you're telling Git that you'd like may like to maintain a copy of the current version of your changes.
     1. Once you've initialized a repository ina folder you may wish to add files that should also also be tracked by Git.
     2. To add all of your changes to staging the command would be ```git add .```
     3. When adding specific changes to staging you'd use ```git add yourFileName.yourFileExtension```
  5. Commiting changes is how you truly maintain a copy of your changes. This stores a version of the changes you've staged into Git, which you may revisit later if needed.
     1. ```git commit```
     2. Each commit will be accompanied by a commit message. This message should give you and other users a short description of the changes that you're saving. When running the command ```git commit``` You'll be asked to enter a commit message in VIM.
     3. If you're unfamiliar with Vim it may behove you to use the command ```git commit -m"YourCommitMessage"``` which will allow you to add your commit message without entering VIM.
  6. Git allows you to take advantage of branches in order to safely work on a project. When initializing a new repository, typically Git will name that branch main or master. That branch is typically the branch where you'd like to place changes that have been tested, and have been considered safe to use in production.
     1. To create a new branch you can use the command ```git checkout -b NewBranchName``` which will create a new branch, and move you to the new branch where you can make experimental changes as you're working.
     2. To checkout any branch you may use ```git checkout branchName``` which will take you to whichever branch you've provided.
     3. To see a list of available branches you can use the command ```git branch```
     4. To switch branches you can also use the commant ```git switch branchName```
     5. Changes made on a new branch will not be tracked on your main branch, after testing you may decide that you like your changes at which point you can merge your changes into your main branch.
        1. Make sure you've commited your changes on the branch you've been testing.
        2. It's best to check for any merge conflicts by meging your master branch into the current branch, this allows you to resolve merge conflicts outside of the master branch. From there you'd switch back to your master branch using some combination of the commands above, then run the command ```git merge workingBranch``` which will merge your updated branch with the master branch. 
7. There are several other operations that can be performed in Git, and it is important to be aware of what each command does, and how to safely use them. I'd advise any readers to spend time familiarizing themselves with the documentation at [Githubs Git guide](https://github.com/git-guides) before working with Git.


