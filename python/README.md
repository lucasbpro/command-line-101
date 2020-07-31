# Command Line 101 - Python

## Setting up a Virtual Environment (venv)

virtualenv is used to manage Python packages for different projects. Using virtualenv allows you to avoid installing Python packages globally which could break system tools or other projects. You can install virtualenv using pip. Refer to [source](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/).

### Installation
```bash  
$ pip install virtualenv
```
### Create venv on Linux/MAC
```bash   
$ virtualenv venv [OR]  virtualenv venv -p <python-version>
$ source venv/bin/activate 
$ pip install -r requirements.txt
```
Para desativar o ambiente virtual:
```bash   
$ deactivate
```
### Create venv on Windows
```bash
> virtualenv ../venv -p <python-version - example: python3>
> ../venv/Scripts/activate
> pip install -r requirements.txt
```
### Create venv by using *conda*
```bash
$ conda create -n venv          
$ conda activate venv   
```
