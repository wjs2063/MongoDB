1. python-3.9.16 설치
2. fast api 설치
3. vim setting
4. pip3 install


yum  y install wget
yum -y install gcc

python https://www.python.org/ftp/python/3.9.16/Python-3.9.16.tgz

```
tar -xvf Python-3.9.16.tgz
cd Python-3.9.16/
./configure --enable-optimizations

make
make install

which python3.9

vim .bashrc
alias python3="/usr/local/bin/python3.9"
source .bashrc

```
