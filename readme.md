// Creation

1 // installation python version 3
2 // creation folder project and a main.py file

3 // Creation virtual enviroment
        "py -3 -m venv env"
4 // going to virtual enviroment power shell
        "& {current file}/env/Scripts/activate.ps1"
5 // update pip
    "python -m pip install --upgrade pip"

6 // installation pylint or other packages
    "pip install pylint"

7 // creation requirment file
    "pip freeze > requirements.txt"
8 // changing interpreter for pylint to enviroment python

    .vscode//setting.json
    {
    "python.pythonPath": "${workspaceFolder}\\env\\Scripts\\python.exe"
    }

9 // changing debugger setting 

    .vscode//launch.json
    {
        "version": "0.2.0",
        "configurations": [
            {
                "name": "Python: Current File (Integrated Terminal)",
                "type": "python",
                "request": "launch",
                "program": "${workspaceFolder}/main.py",
                "console": "integratedTerminal"
            },
        ]
    }
    