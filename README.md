# spaCy tutorial


## Environment dependencies
First, set up a virtual environment for Python 3.x using `virtualenv`:
```
virtualenv -p /usr/bin/python3 ~/venv
pip install --upgrade pip
pip install -r requirements.txt
```

That assumes the Python binary is located at `/usr/bin/python3` --
change that as needed.

Then to activate the environment:
```
source ~/venv/bin/activate
```

## Jupyter launch
To launch a headless Jupyter instance (e.g., running on a remote server in the cloud):
```
nohup jupyter-notebook --no-browser --port=8888 --NotebookApp.token='' --ip='0.0.0.0' &
```