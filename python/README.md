# Python

## Creating Virtual Environment (venv)

### Installation
```bash  
> pip3 install virtualenv
```

### Create venv on Linux/MAC
```bash   
$ virtualenv venv [OR]  virtualenv venv -p <python-version>
$ source venv/bin/activate 
$ pip install -r requirements.txt
& deactivate
```
Para desativar o ambiente virtual:
```bash   
& deactivate
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
