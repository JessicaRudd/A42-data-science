<!-----
NEW: Check the "Suppress top comment" option to remove this info from the output.

Conversion time: 0.378 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β29
* Wed Mar 17 2021 11:57:01 GMT-0700 (PDT)
* Source doc: Data Science Project Checklist
* This is a partial selection. Check to make sure intra-doc links work.
----->




 # Setup
    - [ ] Use cookiecutter to create project template
    ```
       $ conda install -c conda-forge cookiecutter or (pip install cookiecutter) 
       $ cookiecutter [https://github.com/A42labs/A42-data-science](https://github.com/A42labs/A42-data-science)
    ```
        - [ ] Follow prompts to setup project

    - [ ] Change working directory into project folder
    ```
       $ cd project-dir
    ```
    - [ ] Create project environment (I recommend Anaconda as environment manager because it is language agnostic)
        - [ ] Create conda environment from environment.yml file 
        - [ ] Include jupyter, nbextensions (for notebook table of contents and other add-ins), pep8, isort, black, deon, cookiecutter, etc. 