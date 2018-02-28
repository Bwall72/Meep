### Meep provides an out of date installation script
install.sh fixes the package name for python and libpng

To intsall on Ubuntu:

```bash
sudo apt-get install gfortran git gcc g++ make python python3 python-pip 
cd ~/ 
git clone https://github.com/Bwall72/Meep.git
mv ~/Meep/install.sh ~/
chmod +x install.sh
./install.sh
python -m pip install --user numpy scipy matplotlib ipython jupyter pandas symp nose
```

### Testing
```bash
cd ~/install/meep/tests
make flux.cpp
./flux
```
