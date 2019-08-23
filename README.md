# spaCy tutorial


## Environment dependencies

First, set up for Jupyter and Python 3.x
```
sudo bash
apt-get update

apt-get install python-pip python3-pip python-dev python3-dev libevent-dev
apt-get install ipython jupyter-notebook

pushd /usr/bin/

rm -r python
ln -s python3 python

rm -f /etc/boto.cfg

pip install -r requirements.txt

exit
```

That assumes the Python binary is located at `/usr/bin/python3` --
change it as needed.


## Jupyter launch
To launch a headless Jupyter instance (e.g., running on a remote server in the cloud):
```
nohup jupyter-notebook --no-browser --port=8888 --NotebookApp.token='' --ip='0.0.0.0' &
```