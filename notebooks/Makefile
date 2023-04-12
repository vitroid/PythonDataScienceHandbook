ORIGINAL=../../PythonDataScienceHandbook/notebooks
DEST=../../PythonDataScienceHandbook-ja/notebooks
JT= ../../jupyter-translate

all:
	(cd $(ORIGINAL); ls *.ipynb) | xargs make -k


%.ipynb: $(JT)/jupyter_translate.py
	cd $(ORIGINAL); python3 $(JT)/jupyter_translate.py $*.ipynb --language ja --dest_path $(DEST)
	sed -e s@jakevdp/PythonDataScienceHandbook/blob/master@vitroid/PythonDataScienceHandbook/blob/ja@g -I .bak $@
