
Creating an environment
=======================

My first attempt was to try pip install pymc on windows 7; this failed with what looked like some ugly blas pack errors in theano. For this reason I flipped my dual book machine to Ubuntuo 16.04 LTS performed a full system update (which took some time) then git cloned my repo.

My goal was to have a Python3, pymc and matplotlib environment all working nicely with my ipynb files lcoally. Such that I could push these nicely into github for others to use.

I also tried and pull the pymc/pymc docker container; this looked incomplete and when I tryed the simple line below this failed

```
import pymc as pm
```

For this reason I finally opted for a simple Python3 virtual environment locally, created using the following command lines. I wrote a simple run.sh script handles a few setup steps a) activate the python3 venv b) cd into my directory containing my .ipynb files c) launch the jupyter notebook on my chosen port (9999, not the default 8888).


```
$ python3 -m venv bmfh
$ . bmfh/bin/activate
$ pip install pymc
$ pip install jupyter
$ pip install matplotlib
```

Launching Environment
=====================

Two simple steps as below; these could be added to superviso; but not sure that I want this to always run.

```
$ cd <repo home locally>
$ ./run.sh
````
