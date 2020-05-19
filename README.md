# NEPC

<!--[![pipeline status](http://predator.nrl.navy.mil/padamson/nepc/badges/master/pipeline.svg)](http://predator.nrl.navy.mil/padamson/nepc/commits/master)
-->
[![pytest coverage report](https://predator.nrl.navy.mil/padamson/nepc/-/jobs/artifacts/master/raw/pytest.svg?job=pytest)](https://predator.nrl.navy.mil/padamson/nepc/commits/master)
[![sphinx coverage report](https://predator.nrl.navy.mil/padamson/nepc/-/jobs/artifacts/master/raw/sphinx.svg?job=sphinx)](http://132.250.158.124:3838/nepc/doc/)
[![pylint report](https://predator.nrl.navy.mil/padamson/nepc/-/jobs/artifacts/master/raw/pylint.svg?job=pylint)](https://predator.nrl.navy.mil/padamson/nepc/commits/master)

The NRL Evaluated Plasma Chemistry (NEPC) project involves building of a 
database of evaluated electron-scattering cross-sections from various sources as well as 
tools to access and visualize the data. Data can be accessed, raw and formatted, through the 
"data" directory, while other directories of the project are used for builing and accessing 
the database. For more information on how the project is organized, please see the 
[Wiki](http://predator.nrl.navy.mil/padamson/nepc/wikis/home). This database is designed 
for anyone interested in plasma chemistry with a background in physics at the graduate level.

## Getting Started

NEPC works best within a conda environment (`environment.yml` file provided). Also, if you are going to build the
database yourself, you will need MySQL. To get started:

```console
$ git clone predator.nrl.navy.mil/padamson/nepc/
$ cd nepc
$ conda env create -f environment.yml #create the nepc conda environment 
$ conda activate nepc
$ pip install -e . #install the nepc package and sub-packages into the nepc conda environment
$ pytest tests/test_nepc.py #verify it works
```

## Built With

*  [Python](https://www.python.org/) 
*  [Jupyter Notebook](https://jupyter.org/)
*  [LaTeX](https://www.latex-project.org/)
*  [MySQL](https://www.mysql.com/)

## MySQL config

```sql
GRANT USAGE ON *.* TO `nepc`@`localhost` 
GRANT SELECT ON `nepc`.* TO `nepc`@`localhost`    
GRANT SELECT ON `nepc_test`.* TO `nepc`@`localhost` 
```
