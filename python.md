## Python Commands

00.	  CNTL + Z (terminate the python shell)
01.   `brew install pipenv` (installs pipenv, something roughly equivalent to npm for node)
2.    `python` (opens `>>>` prompt to execute python commands)
3.    `curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py` (downloads pip package manager for python)
4.    `python get-pip.py` (runs pip you just download in above step)
5.    `python -m venv env` (creates a virtual environment inside of whatever folder you start it in, python 3)
6.    `source env/bin/activate` (activates your virtual environment)
7.    `deactivate` (stops your virtual environment)
8.    `pip install virtualenvwrapper` (gives you another set of virtual environment tools to work with)
9.    `mkvirtualenv your-environment-here` (if using `virtualenvwrapper`, this starts up)
10.   `workon your-environment-here` (takes your environment and makes the virtual one for you - make sure you're in the right folder)