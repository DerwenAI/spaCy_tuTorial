# spaCy 튜토리얼 (spaCy tuTorial)

## 안내사항 (Instructions)

이 튜토리얼은 구글 코랩(Google Colab)의 주피터 노트북(Jupyter notebooks) 환경에서 실행되도록 제작되었습니다.
자세한 내용은 <https://derwen.ai/s/d5c7>의 슬라이드를 참고하세요.
[![Google Colab](https://badgen.net/badge/Launch/on%20Google%20Colab/blue?icon=terminal)](https://colab.research.google.com/github/DerwenAI/spaCy_tuTorial/blob/master/Text_Rank.ipynb)

## 환경 종속성 (Environment dependencies)

구글 코랩(Google Colab)에서 실행하지 않는 경우, 먼저 주피터(Jupyter)와 파이썬 3(Python 3.x) 버전을 위한 GCP(구글 클라우드 플랫폼) 환경을 설정하세요:
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

이 설정은 파이썬 실행 파일(binary)이 `/usr/bin/python3` 경로에 있다는 것을 가정합니다. 필요에 따라 경로를 변경하세요.

그다음, 공식 사이트에서 `conda`를 설치하세요.
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

## 주피터 실행(Jupyter launch)
다음 명령어를 반드시 실행하세요:
```
source ~/.bashrc
```

그다음, 헤드리스(headless) 주피터 인스턴스를 실행하려면 (예: 클라우드의 원격 서버에서 실행할 경우) 다음 명령어를 입력하세요:
```
nohup ~/anaconda3/bin/jupyter notebook --no-browser --port=8888 --NotebookApp.token='' --ip='0.0.0.0' &
```
