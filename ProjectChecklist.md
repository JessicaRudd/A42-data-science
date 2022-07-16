# Data Science Project Checklist

- [ ] Setup (these are MacOS specific instructions)
    - [ ] Install and setup Pyenv for installing and managing Python versions
      - [ ] Install command line tools
        ```
        xcode-select --install
        ```
      - [ ] Install Homebrew package manager
        ```
        /bin/bash -c “$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
        ```
      - [ ] Install dependcies
        ```
        brew install openssl readline sqlite3 xz zlib
        ```
      - [ ] Install pyenv
        ```
        brew install pyenv
        ```
      - [ ] Add pyenv to your PATH by updating .zshrc file
        ```
        echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
        echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
        echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.zshrc
        ```
      - [ ] Close and reload terminal to pickup changes
      - [ ] Pyenv commands
        ```
        # Show list of available Python versions
        pyenv install --list

        # Install Python version
        pyenv install {version} # can install any version available from the available list

        # Check currently installed Python versions
        pyenv versions

        # Set a particular version as default global version
        pyenv global {version}

        # To set a particular version in a project, navigate to the project directory and:
        pyenv local {version}
        ```
    - [ ] Cookiecutter to create project template - follow prompts to setup project
        ```
        ## Install cookiecutter package
        pip install cookiecutter

        ## Start a new cookiecutter project based off of this template
        cookiecutter https://github.com/JessicaRudd/A42-data-science
        ``` 
    - [ ] Change into new project folder 
        ```
        cd project-dir
        ```
    - [ ] Initialize Git repository 
        ```
        git init
        ``` 
        - There's a great explanation of creating a git repository, pushing to Github, and other tasks for creating a reproducible project [here](https://www.dataquest.io/blog/how-to-share-data-science-portfolio/), or this from [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
        - [ ] Download GitHub CLI for additional git and Github capabilities from within the command line (rather than context switching between CLI and Github in web browser or Github Desktop)
            - [ ] macOS: 
                ```
                brew install gh
                ```
            - [ ] Windows:
                ```
                winget install gh
                ```
    
        - [ ] Create new GitHub repository from GitHub CLI
                ```
                gh repo create
                ```
        - [ ] Git add, commit, push to the new remote repository 
    
                ```
                git add .

                git commit -m "add commit message here"

                git push origin main
                ```
            - Good commit messages are important for documenting source control and adding valuable context to your work (both for future you and for your collaborators!)
            - Check out [this source](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/) and [this source](https://hackernoon.com/7-rules-for-writing-a-good-commit-message?source=rss) for tips on writing good commit messages.
        - The cookiecutter project template automatically creates a .gitignore file for you but you can create one from a template [here](https://github.com/github/gitignore/blob/master/Python.gitignore). This is a good idea so extraneous files, secret keys, etc. are not shared publicly via git. 
    - [ ] Create project environment 
        ```
        ## Uses Makefile to setup the virtual environment for development
        make venv
        ```
        - [ ] Activate environment
            ```
            source venv env/bin/activate
            ```
        - [ ] Deactivate environment when done working on project:
            ``` 
            deactivate
            ```
    - [ ] Pre-commit framework (automatically included in this cookiecutter template)
        - [ ] Pre-commit hooks can be used to check for clean code conventions before committing changes - isort, black, flake
            - This is best used on python scripts rather than the development jupyter notebooks since it will help with CI/CD framework
    - [ ] Install ethics checklist markdown file with deon and/or append to script (the markdown ethics file is automatically included in the [A42 Data Science CookieCutter template](https://github.com/JessicaRudd/A42-data-science))
    - [ ] This code [reproducibility checklist](https://www.cs.mcgill.ca/~jpineau/ReproducibilityChecklist.pdf) should also be considered
    - [ ] Add secret keys from required APIs, logins, etc. to the .env file in project directory (make sure .env is added to the .gitignore file if not already)
        - [ ] Use python-dotenv to load secret keys from environment into python script when sharing the project (basic how-to found [here](https://mathdatasimplified.com/2021/02/20/python-dotenv-how-to-load-the-secret-information-from-env-file/))
