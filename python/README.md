# Command Line 101 - Python

## Setting up a Virtual Environment (venv)

_virtualenv_ is used to manage Python packages for different projects. Using virtualenv allows you to avoid installing Python packages globally which could break system tools or other projects. You can install virtualenv using pip. Refer to [this documentation](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/).

### Installation
```bash  
$ pip install virtualenv
```
### Create venv on Linux/MAC
```bash   
$ virtualenv venv 
$ source venv/bin/activate 
$ pip install -r requirements.txt
```
Or by specifying a specific python version (for example, Python 3.6):
```bash   
$ virtualenv venv -p python3.6
$ source venv/bin/activate 
$ pip install -r requirements.txt
```
To deactivate the virtual environment:
```bash   
$ deactivate
```
### Create venv on Windows
```bash
$ virtualenv ../venv -p python3
$ ../venv/Scripts/activate
$ pip install -r requirements.txt
```
### Create venv by using *conda*
```bash
$ conda create -n venv          
$ conda activate venv   
```
