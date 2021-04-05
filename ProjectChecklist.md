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
    - [ ] change into new project folder 
    ```
    cd project-dir
    ```
    - [ ] Create project environment (I recommend Anaconda as environment manager since it is language agnostic)
        - [ ] Create conda environment from environment.yml file --> can create a base environment file to re-use and/or add project specific requirements
        - [ ] Suggestions: include jupyter, nbextensions (for notebook table of contents and other useful add-ins), pep8, isort, black, deon
        

