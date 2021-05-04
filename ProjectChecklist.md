# Data Science Project Checklist

- [ ] Setup
    - [ ] Cookiecutter to create project template \
        \
        For conda install
    
        ``` 
        conda install -c conda-forge cookiecutter
        ```
        For pip install 
        ```
        pip install cookiecutter
        ```
        Follow prompts to setup project 
    - [ ] Change into new project folder 
        ```
        cd project-dir
        ```
    - [ ] Create project environment (I recommend Anaconda as environment manager since it is language agnostic)
        - [ ] Create conda environment from environment.yml file --> can create a base environment file to re-use and/or add project specific requirements
        - [ ] Suggestions: include jupyter, nbextensions (for notebook table of contents and other useful add-ins), pep8, isort, black, deon
        [Example environment.yml file](https://github.com/binder-project/example-conda-environment/blob/master/environment.yml)

        - [ ] Search for environment.yml file and create environment from that file
            ```
            conda env create
            ```
        - [ ] Activate environment
            ```
            conda activate {env name}
            ```
        - [ ] If project dependencies added/updated, update environment.yml 
            ```
            nano environment.yml
            ```
            then
            ```
            conda env update --file environment.yml --prune
            ```
        - [ ] Deactivate environment when done working on project:
            ``` 
            conda deactivate
            ```

    - [ ] Initialize Git repository 
            ```
            git init
            ``` 
            \
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
                ```E
        - The cookiecutter project template automatically creates a .gitignore file for you but you can create one from a template [here](https://github.com/github/gitignore/blob/master/Python.gitignore). This is a good idea so extraneous files, secret keys, etc. are not shared publicly via git. 
    - [ ] Pre-commit framework
        - [ ] Pre-commit hooks can be used to check for clean code conventions before committing changes - isort, black, flake
            - This is best used once you have packaged source code rather than the development jupyter notebooks since it will help with CI/CD framework
        - [ ] Can also make a simple formatting script and run before commits:
            [autoformat template](https://github.com/G-Hung/model-productization_article/blob/master/autoformat.sh)
            Then run:
            ```
            ./autoformat.sh
            ```
            If you get a permission error, first run:
            ```
            chmod +rx autoformat.sh
            ```
    - [ ] Install ethics checklist markdown file with deon and/or append to script (the markdown ethics file is automatically included in the [A42 Data Science CookieCutter template](https://github.com/a42labs/A42-data-science))
    - [ ] This code [reproducibility checklist](https://www.cs.mcgill.ca/~jpineau/ReproducibilityChecklist.pdf) should also be considered
    - [ ] Add secret keys from required APIs, logins, etc. to the .env file in project directory (make sure .env is added to the .gitignore file if not already)
        - [ ] Use python-dotenv to load secret keys from environment into python script when sharing the project (basic how-to found [here](https://mathdatasimplified.com/2021/02/20/python-dotenv-how-to-load-the-secret-information-from-env-file/))
