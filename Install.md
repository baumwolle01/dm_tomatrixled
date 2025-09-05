Install:

1.
sudo apt update && sudo apt upgrade -y
sudo apt install -y git python3 python3-pip build-essential libgraphicsmagick++-dev cython3 python3-dev

2.
cd ~
git clone https://github.com/baumwolle01/dm_tomatrixled.git
cd dm_tomatrixled

3.
pip3 install -r requirements.txt
Alt:
pip3 install requests Pillow

4.
cd ~/dm_tomatrixled
git clone https://github.com/hzeller/rpi-rgb-led-matrix.git
cd rpi-rgb-led-matrix/bindings/python
make build-python PYTHON=$(which python3)
sudo make install-python

5. Test:
sudo python3 dm_tomatrixled.py -s de:05111:18036:8:2 -e --led-rows 16
