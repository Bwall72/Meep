### Meep provides an out of date installation script
install.sh fixes the package name for python and libpng

To intsall on Ubuntu:

##### Meep

```bash
sudo apt-get install gfortran git gcc g++ make python python3 python-pip 
cd ~/ 
git clone https://github.com/Bwall72/Meep.git
mv ~/Meep/install.sh ~/
chmod +x install.sh
./install.sh
```
##### To use the Pyhton library

```bash
python -m pip install --user numpy scipy matplotlib ipython jupyter pandas symp nose
wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda.sh
bash miniconda.sh
exit
```
Terminal needs to be reset after running miniconda.sh

```bash
conda create -n mp -c chogan -c defaults -c conda-forge pymeep
conda create -n mp -c chogan -c defaults -c conda-forge pymeep-parallel
```

Before running python script activate either 
pymeep environment:
```bash
source activate mp
```
or pymeep parallel environment
```bash
source activate pmp
```


### Testing

##### C++:
```bash
cd ~/install/meep/tests
make flux.cpp
./flux
```
##### Python
