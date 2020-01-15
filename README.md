# Version Control with Git
https://swcarpentry.github.io/git-novice/  

## Workshop Intro

### Comments
During lesson feel free to comment and ask questions at any time.  

### Expectations
* Avoid rabbit holes
* Read the error messages
* “Learners frequently report that the most valuable part of the workshop is seeing the instructors’ mistakes and how they diagnose and fix them” Wilson (2014)

### What Not to Put Under Version Control 
Wilson et al. (2016)  
The benefits of version control systems don't apply equally to all file types. In particular, version control can be more or less rewarding depending on file size and format. First, file comparison in version control systems is optimized for plain text files, such as source code. The ability to see so-called "diffs" is one of the great joys of version control. Unfortunately, Microsoft Office files (like the .docx files used by Word) or other binary files, e.g., PDFs, can be stored in a version control system, but it is not possible to pinpoint specific changes from one version to the next. Tabular data (such as CSV files) can be put in version control, but changing the order of the rows or columns will create a big change for the version control system, even if the data itself has not changed.  

Second, raw data should not change, and therefore should not require version tracking. Keeping intermediate data files and other results under version control is also not necessary if you can re-generate them from raw data and software. However, if data and results are small, we still recommend versioning them for ease of access by collaborators and for comparison across versions.  

Third, today's version control systems are not designed to handle megabyte-sized files, never mind gigabytes, so large data or results files should not be included. (As a benchmark for "large", the limit for an individual file on GitHub is 100MB.) Some emerging hybrid systems such as Git LFS26 put textual notes under version control, while storing the large data itself in a remote server, but these are not yet mature enough for us to recommend.  

### Inadvertent Sharing  
Researchers dealing with data subject to legal restrictions that prohibit sharing (such as medical data) should be careful not to put data in public version control systems. Some institutions may provide access to private version control systems, so it is worth checking with your IT department.  

Additionally, be sure not to unintentionally place security credentials, such as passwords and private keys, in a version control system where it may be accessed by others.

## Terminology  
Git = program that runs locally on a computer  
Github = cloud based git service, includes added features and services


Companies that support Git besides Github:  
https://bitbucket.org/product  
https://cloud.google.com/source-repositories/  
https://azure.microsoft.com/en-us/services/devops/repos/  
https://aws.amazon.com/codecommit/  

## Required Setup  
To participate in a Software Carpentry workshop, you will need access to the software described below. In addition, you will need an up-to-date web browser.  

We maintain a list of common issues that occur during installation as a reference for instructors that may be useful on the Configuration Problems and Solutions wiki page.  

### The Bash Shell
Bash is a commonly-used shell for doing simple tasks using typed commands.

### Windows
1. Download the Git for Windows installer.
1. Run the installer and follow the steps bellow:
   1. Click on "Next".
   1. Click on "Next".
   1. Keep "Use Git from the Windows Command Prompt" selected and click on "Next". If you forgot to do this programs that you need for the workshop will not work properly. If this happens rerun the installer and select the appropriate option.
   1. Click on "Next".
   1. Keep "Checkout Windows-style, commit Unix-style line endings" selected and click on "Next".
   1. Keep "Use Windows' default console window" selected and click on "Next".
   1. Click on "Install".
   1. Click on "Finish".
1. If your "HOME" environment variable is not set (or you don't know what this is):
   1. Open command prompt (Open Start Menu then type cmd and press [Enter])
   1. Type the following line into the command prompt window exactly as shown:
   1. setx HOME "%USERPROFILE%"
   1. Press [Enter], you should see SUCCESS: Specified value was saved.
   1. Quit command prompt by typing exit then pressing [Enter]

This will provide you with both Git and Bash in the Git Bash program.

### Mac OS X  
The default shell in all versions of Mac OS X is Bash, so no need to install anything. You access Bash from the Terminal (found in /Applications/Utilities). See the Git installation video tutorial for an example on how to open the Terminal. You may want to keep Terminal in your dock for this workshop.  

### Linux
The default shell is usually Bash, but if your machine is set up differently you can run it by opening a terminal and typing bash. There is no need to install anything.

### Git Program  
Git is a version control system that lets you track who made changes to what when and has options for easily updating a shared or public version of your code on github.com. You will need a supported web browser (current versions of Chrome, Firefox or Safari, or Internet Explorer version 9 or above).  

You will need an account at github.com for parts of the Git lesson. Basic GitHub accounts are free. We encourage you to create a GitHub account if you don't have one already. Please consider what personal information you'd like to reveal. For example, you may want to review these instructions for keeping your email address private provided at GitHub.

#### Windows
Git should be installed on your computer as part of your Bash install (described above).  

#### Mac OS X
For OS X 10.9 and higher, install Git for Mac by downloading and running the most recent "mavericks" installer from this list. After installing Git, there will not be anything in your /Applications folder, as Git is a command line program. For older versions of OS X (10.5-10.8) use the most recent available installer labelled "snow-leopard"available here.  

#### Linux
If Git is not already available on your machine you can try to install it via your distro's package manager. For Debian/Ubuntu run sudo apt-get install git and for Fedora run sudo yum install git.

### Text Editor  
When you're writing code, it's nice to have a text editor that is optimized for writing code, with features like automatic color-coding of key words. The default text editor on Mac OS X and Linux is usually set to Vim, which is not famous for being intuitive. if you accidentally find yourself stuck in it, try typing the escape key, followed by :q! (colon, lower-case 'q', exclamation mark), then hitting Return to return to the shell.

#### Windows  
nano is a basic editor and the default that instructors use in the workshop. To install it, download the Software Carpentry Windows installer and double click on the file to run it. This installer requires an active internet connection.
Others editors that you can use are Notepad++ or Sublime Text. Be aware that you must add its installation directory to your system path. Please ask your instructor to help you do this.

#### Mac OS X  
nano is a basic editor and the default that instructors use in the workshop. See the Git installation video tutorial for an example on how to open nano. It should be pre-installed.
Others editors that you can use are Text Wrangler or Sublime Text.

#### Linux  
nano is a basic editor and the default that instructors use in the workshop. It should be pre-installed.
Others editors that you can use are Gedit, Kate or Sublime Text.

## Git Client Software  
List of Clients, +30:
https://git-scm.com/downloads/guis/

### Tortoise Git  
Windows Explorer icon overlays and context menus
https://tortoisegit.org/


### GitKraken
  
Stand alone application for repository management
https://www.gitkraken.com/

### Matlab  
Matlab has git integration in the Workspace view.


### Spyder3 IDE for Python  
Uses Git GUI
Note UI will not selectively stage changes - items must be ignored or added.
https://www.spyder-ide.org/


### Gitk  
Graphical history viewer, like the command `git log`  

### KDiff (TortoiseGitMerge)    


### RStudio
https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN
### Sublime Text
https://www.sublimetext.com/docs/3/git_integration.html

## Ways to Use Git  
### Docker Build Files  
https://docs.docker.com/engine/reference/commandline/build/  
https://stackoverflow.com/questions/26753030/how-to-build-docker-image-from-github-repository  

### Conda Environment Files  
https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html  

### Python PIP Requirements Files
https://pip.pypa.io/en/stable/user_guide/#requirements-files  

### R packrat  
https://rstudio.github.io/packrat/  

### Machine Learning Models  
https://dvc.org/  
https://blog.algorithmia.com/how-to-version-control-your-production-machine-learning-models/  

## Git Concepts  
Introduction to the Unix Shell  
The following is from the first 3 sections of:  
http://swcarpentry.github.io/shell-novice/  

### Bash Concepts
* $ = prompt
* Tab to use completions
* Up arrow to reuse previous commands
* Paste
* ctrl + insert_key (windows)
* shift + ctrl + v (linux)
* apple + v (mac)
* Read-Evaluate-Print Loop (REPL)


#### Bash Commands

help  
pwd  
ls  
ls -a  
cd  
cd ..  
mkdir  
$ mkdir <dir_name>  
rm  
$ rm <file>  
rm -d  
$ rm -d <dir_name>   
nano  

## Version Control with Git and Bash  

Create your own planets repo by follow along here:  
http://swcarpentry.github.io/git-novice/  

### Git Command syntax    

help  

```git <command> --help```  
or  
```git help <command>```  

Example:
```git commit --help```  
  
### Local Operations  
```
git config  
git init  
git status  
git add  
git commit  
git log  
git diff  
git checkout  
```

#### The .gitignore file

#### Remote Operations  
```
git push  
git pull  
git clone  
```

Example Repo for cloning:


## Gotchas
1. Pasting Clone links into Git Bash can copy unsupported characters  
2. Newline checkouts and commits vary across operating systems, see: https://help.github.com/articles/dealing-with-line-endings/  

## Future Study  

`fork` = make your own copy of another repo  
`merge` = combine two repo versions of a file  
`branch` = make a version local to the current repo (vision quest)  
`pull request` = ask owner of an repo to pull your repo into theirs  

Syntax for private repos = (SSH keys, 2 factor auth, tokens)  

## Revision Control in the Wild  
https://docs.scipy.org/doc/numpy/dev/  
http://developer.r-project.org/  
https://scikit-learn.org/stable/developers/contributing.html  
https://golang.org/doc/contribute.html  

## Background on Software Carpentry  
NIST Training Example  
https://pages.nist.gov/2018-09-11-nist/  

Wilson (2014) Software Carpentry: Lessons Learned  
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3976103/  

Wilson et al. (2014) Best Practices for for Scientific Computing  
https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1001745  

Wilson et al. (2016) Good Enough Practices in Scientific Computing  
https://arxiv.org/abs/1609.00037  
