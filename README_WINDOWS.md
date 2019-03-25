# setup environment
install python3.7 from https://www.python.org/downloads/  
pip install virtualenv  

# start virtual environment
cd D:\project  
virtualenv venv  
cd venv\Scripts  
activate

# download sonic-snmpagent-dev
cd D:\project  
git clone https://github.com/Kason-Peng/sonic-snmpagent-dev  
cd sonic-snmpagent-dev  
git submodule init  
git submodule update  

# install sonic dependency
cd sonic-py-swsssdk  
python setup.py build  
python setup.py install  
cd ../sonic-snmpagent  
python setup.py build  
python setup.py install  

# install test dependency
pip install mockredispy  
