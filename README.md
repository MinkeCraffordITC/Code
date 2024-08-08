# Developer Cheat sheet
______________________________________________

1. To use Rye you need to have a pyproject.toml based Python project
  - rye init project_name
  - cd project_name

The following structure will be created:

![image](https://github.com/user-attachments/assets/8f2f5d76-0763-4832-9fd2-bb4bd1f587bf)
![image](https://github.com/user-attachments/assets/bf862512-6da2-469f-979c-89e0a9ce0476)

2. First Sync
  - rye sync
    - Rye will created the following: 
    - virtualenv in .venv
    - written lockfiles into requirements.lock and requirements-dev.lock 

3. Adding Dependencies
  - rye add "dependency>=version"
    - rye sync
      - to install the dependency into the virtual environment

4. Listing Dependencies
  - rye list
    - get a dump of all installed dependencies of your project

5. Remove a Dependencies
  - rye remove dependency
    -  remove a dependency from the project again

6. Working with the Project
  - rye run ruff [example]
    - run executables

Step 2, 3 and 6 [example]:

![image](https://github.com/user-attachments/assets/7b336945-c860-48c3-a359-dc5e6858a073)


7. Inspecting the Project
  - rye show
    - print out information about the project's state

  
12. Executable projects
  - to generate a project that is aimed to provide an executable script, use rye init --script:
    - rye init --script my-project
    - cd my-project
   
The following structure will be created:

![image](https://github.com/user-attachments/assets/219dbb6d-b868-4b5c-9bcb-d381aa6e524b)


The pyproject.toml will be generated with a [project.scripts] section containing a project_name script that points to the main() function of __init__.py. 
After you synchronized your changes, you can run the script with rye run project_name
  - rye sync
  - rye run project_name
