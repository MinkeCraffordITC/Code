# Developer Cheat sheet
______________________________________________

## Rye

1. To use Rye you need to have a pyproject.toml based Python project
  - *rye init project_name*
  - *cd project_name*

The following structure will be created:

![image](https://github.com/user-attachments/assets/8f2f5d76-0763-4832-9fd2-bb4bd1f587bf)

#### Note!
The init command accepts a lot of options to customize what it generates.
  - Run  *rye init --help*  to see all the options available in the version you have installed.

2. First Sync
  - *rye sync*
    - Rye will created the following: 
    - virtualenv in .venv
    - written lockfiles into requirements.lock and requirements-dev.lock 

3. Adding Dependencies
  - *rye add "dependency>=version"*
    - *rye sync*
      - to install the dependency into the virtual environment

4. Listing Dependencies
  - *rye list*
    - get a dump of all installed dependencies of your project

5. Remove a Dependencies
  - *rye remove dependency*
    -  remove a dependency from the project again

6. Working with the Project
  - *rye run ruff* (example)
    - runs executables

Step 2, 3 and 6 (example):

![image](https://github.com/user-attachments/assets/7b336945-c860-48c3-a359-dc5e6858a073)


7. Inspecting the Project
  - *rye show*
    - print out information about the project's state

  
8. Executable projects
  - to generate a project that is aimed to provide an executable script, use *rye init --script*:
    - *rye init --script my-project*
    - *cd my-project*
   
The following structure will be created:

![image](https://github.com/user-attachments/assets/219dbb6d-b868-4b5c-9bcb-d381aa6e524b)

#### Note!
The pyproject.toml will be generated with a [project.scripts] section containing a project_name script that points to the main() function of __init__.py. 
After you synchronized your changes, you can run the script with rye run project_name
  - *rye sync*
  - *rye run project_name*

### Commands
This is a list of all the commands that rye provides:

- *add*: Adds a Python package to this project
- *build*: Builds a package for distribution
- *config*: Reads or updates the Rye configuration
- *fetch*: Fetches a Python interpreter for the local machine (alias)
- *fmt*: Run the code formatter on the project
- *init*: Initializes a new project
- *install*: Installs a global tool (alias)
- lock: Updates the lockfiles without installing dependencies
- *lint*: Run the linter on the project
- *make-req*: Builds and prints a PEP 508 requirement string from parts
- *pin*: Pins a Python version to the project
- *publish*: Publish packages to a package repository
- *remove*: Remove a dependency from this project
- *run*: Runs a command installed into this package
- *show*: Prints the current state of the project
- *sync*: Updates the virtualenv based on the pyproject.toml
- *test*: Runs the project's tests
- *toolchain*: Helper utility to manage Python toolchains
- *tools*: Helper utility to manage global tools.
- *self*: Rye self management
- *uninstall*: Uninstalls a global tool (alias)
- *version*: Get or set project version

## Python

1. Python Libraries
  - polars
  - rich

2. Python Formatter
  - ruff (using)
  - black

3. Python Linter
  - pylance

4. AI 
  - chatgpt (general)
  - github copilot (coding)
  - sourcery 
