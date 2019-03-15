# download sonic-snmpagent
git clone https://github.com/Azure/sonic-snmpagent  

# setup environment
sudo apt-get update  
sudo apt-get install python3-setuptools  
sudo apt-get install python3-dev  
sudo apt-get install python3-pip  

# install sonic dependency
git clone https://github.com/Azure/sonic-py-swsssdk  
cd sonic-py-swsssdk  
sudo python3.5 setup.py install  
cd sonic-snmpagent  
sudo python3.5 setup.py install  

# install test dependency
pip3 install mockredispy  
pip3 intestll pytest  
