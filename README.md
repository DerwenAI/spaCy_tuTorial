# spaCy tutorial


## Environment dependencies

First, set up for Jupyter and Python 3.x
```
sudo bash
apt-get update
apt-get install virtualenv python-pip python3-pip
apt-get install python-dev python3-dev libevent-dev
apt-get install ipython

pushd /usr/bin/
rm -r python
ln -s python3 python
rm -f /etc/boto.cfg
exit
```

That assumes the Python binary is located at `/usr/bin/python3` --
change it as needed.

Then set up a virtual environment for Python 3.x using `virtualenv`:
```
virtualenv -p /usr/bin/python3 ~/venv
pip install -r requirements.txt
```

On each login, activate the environment:
```
source ~/venv/bin/activate
```

## Jupyter launch
To launch a headless Jupyter instance (e.g., running on a remote server in the cloud):
```
nohup jupyter-notebook --no-browser --port=8888 --NotebookApp.token='' --ip='0.0.0.0' &
```