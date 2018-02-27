### Meep provides an out of date installation script
install.sh fixes the package name for python and libpng

To intsall on Ubuntu:

```bash
sudo apt-get install gfortran git gcc g++ make 
cd ~/ 
git clone https://github.com/Bwall72/Meep.git
mv ~/Meep/install.sh ~/
chmod +x install.sh
./install.sh
```

### Testing
```bash
cd ~/install/meep/tests
make flux.cpp
./flux
```
