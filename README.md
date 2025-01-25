# ED Handbook
The new central guide webpage for the video game Elite: Dangerous.
This is the project repository for the Handbook project.
A New Website Name and Logo will be chosen later on by the development community.

## Getting Github Desktop and an Account
Let's get some software downloaded and an account for Github. If you want a code-free environment to upload and download stuff from our Github Repository, instead of doing it manually, one great option is to use Github Desktop. You just need to understand some basic functions

* [Github Desktop](https://desktop.github.com/download/)
* [Github Account](https://github.com/signup)

After you've signed up to a Github Account, please message me your username. Usernames are **case sensitive** so please make sure you have the right username. 

## Downloading Project into Local Environment
You'll need to have the latest installations after being invited into the Repository:

* [Latest Python Version](https://www.python.org/downloads/)
* A Development Environment such as [Visual Studio Code](https://code.visualstudio.com/download)
* NotePad++ can also be used, but for convenience and practicality, Visual Studios is preferred.

Let's open up Github Desktop and find the Repository to "Clone". **Clone** just means to download the project from this repository down into your local folder as is, without the hosting environment.

From File, go to Clone Repository. Choose from ED-Handbook and the folder of the repository and clone the project. You may save this to any file that is easy to access. A recommendation is to save it directly under this path:

```
C:\Users\yourusername\
```

## Setting Up the Local Environment

Let's setup the local environment. Let's open up a command line. For starters, command line will open up to this path `C:\Users\yourusername\`. 

1. Let's use `dir` to check that if our repository is cloned correctly. You should find "ED-Handbook" within the list of other folders in the same path. 
2. Excellent, let's then use `cd ED-Handbook` to enter into the folder of our project.
3. Then, we need to use Python's PIP command to install Material by MKDocs. Use `pip install mkdocs-material` and wait for the package to be installed. 

### For Programmers

It is in good practice to setup a virtual environment in case we need to control dependencies within our project. Let's start at 3. from the setting up the environment.

If you are **not a programmer** and is solely using this to edit markdown files, you can skip to **step 6**.

4. You will do `python -m venv venv` to create a new environment.
5. Then we need to activate the Virtual Environment's Script. Use `.\venv\Scripts\activate\`.
* If you run into an Execution Policy error, we'll do the following to get sorted. Use ` Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser` and then Press "Y" to continue. Rerun the activation program to run the virtual environment.

6. Great, you should have a basic environment built for the project, you can now begin editing. Let's open up Visual Studios by using the command `code .`

### For Programmers

If you are **not a programmer** and is solely using this to edit markdown files, you can skip to **step 7**.

7. In Visual Studios Code, we'll launch the Virtual Environment again just to check that things are in order, again, if you run into Execution Policy errors, refer to **Steps 4 & 5**. Use `.\venv\Scripts\activate\`.

8. Let's open up a new Terminal from within Visual Studios. This can be found at the top of the program. In this terminal, you should see the path be set to `C:\Users\yourusername\ED-Handbook\`. Let's use `dir` to make sure everything is right before using `mkdocs serve` to launch the project into your [localhost](http://127.0.0.1:8000/).

Awesome! That should be it. 

## Deploying Changes into Local Environment

Deploying changes you made to reflect how the page should look from your localhost address is as easy as saving the document. `mkdocs serve` will automatically deploy the changes and reflect this into your localhost. 

If you add a new Markdown file and do not see the file in the navigations, we would need to address the file in the project's only `.yml` file. We call this the "YAML" file. Head down to the `Nav:` section and add a new Navigations Page Name and link it to the file name of that markdown file.

For example, if a page about Exploration was made, the markdown file is called "exploration.md". If you are unsure about how to point to the page name, you may put the YAML file into the same level as the other **home** and **about** page line. The developers will integrate it later. 
* If you wish to directly add these pages into their subsection, please let one of the developers know and so we can help you out. 

```yml
Nav:
    - Home: index.md
    - About: about.md
    - Guides:
        ...
        ...
    
    - Exploration : exploration.md
```

## Commiting Changes into the Repository

For now, until the website's been hosted, you may commit changes into the Repository. Let's open Github Desktop. Github Desktop will reflect any saved changes you made to a file or several files. Once all of the changes are reviewed, add a commit title, and a small comment if needed.

Then click on **Commit to main** on the very bottom of the page to commit the changes into the repository. 

