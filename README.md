# setup environment
sudo apt-get install python3-pip  
sudo apt-get install python3-venv  

# start virtual environment
pyvenv virenv  
source virenv/bin/activate  

# download sonic-snmpagent-dev
git clone https://github.com/Kason-Peng/sonic-snmpagent-dev  
cd sonic-snmpagent-dev  
git submodule init  
git submodule update  

# install sonic dependency
cd sonic-py-swsssdk  
python3.5 setup.py build  
python3.5 setup.py install  
cd ../sonic-snmpagent  
python3.5 setup.py build  
python3.5 setup.py install  

# install test dependency
pip3 install mockredispy  
