# Python

## Creating Virtual Environment

Installation:
```bash  
> pip3 install virtualenv
```

Create venv on Linux/MAC:
```bash   
$ virtualenv venv [OR]  virtualenv venv -p <python-version - example: python3>
$ source venv/bin/activate 
$ pip install -r requirements.txt
& deactivate    para desativar o venv
```
Create venv on Windows:
```bash
> virtualenv ../venv -p <python-version - example: python3>
> ../venv/Scripts/activate
> pip install -r requirements.txt
```
Create venv by using *conda*:
```bash
$ conda create -n <nome_ambiente>          
$ conda activate <nome_ambiente>      
```