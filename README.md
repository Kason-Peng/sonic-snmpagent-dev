# download sonic-snmpagent
git clone https://github.com/Azure/sonic-snmpagent    

# setup environment
sudo apt-get install python3-pip  
sudo apt-get install python3-venv  

# start virtual environment
pyvenv virenv  
source virenv/bin/activate  

# install sonic dependency
git clone https://github.com/Azure/sonic-py-swsssdk  
cd sonic-py-swsssdk  
python3.5 setup.py build  
python3.5 setup.py install  
cd ../sonic-snmpagent  
python3.5 setup.py build  
python3.5 setup.py install  

# install test dependency
pip3 install mockredispy  
