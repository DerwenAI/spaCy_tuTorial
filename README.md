# spaCy tuTorial

## Instructions

This is built to run in Jupyter notebooks on Google Colab.
See the slides at <https://derwen.ai/s/d5c7> for details.

## Environment dependencies

If you're not running on Google Colab, first for GCP set up for Jupyter and Python 3.x:
```
sudo bash
apt-get update
apt-get install python-dev python3-dev

pushd /usr/bin/
rm -r python
ln -s python3 python

rm -f /etc/boto.cfg

exit
```

That assumes the Python binary is located at `/usr/bin/python3` --
change it as needed.

Then install `conda` from its site.

```
conda install -c conda-forge spacy

python -m spacy download en_core_web_sm
#python -m spacy download en_core_web_md
#python -m download en_core_web_lg
python -m spacy validate

conda install -c conda-forge scattertext
conda install -c anaconda beautifulsoup4

pip install spacy-wordnet

#pip install spacy-transformers
#python -m spacy download en_trf_bertbaseuncased_lg
```

## Jupyter launch

Be sure to:
```
source ~/.bashrc
```

Then to launch a headless Jupyter instance (e.g., running on a remote server in the cloud):
```
nohup ~/anaconda3/bin/jupyter notebook --no-browser --port=8888 --NotebookApp.token='' --ip='0.0.0.0' &
```
