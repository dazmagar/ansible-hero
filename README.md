# Create python venv, setup requirements
```
python -m venv venv
pip install -r requirements
```
# Additional installations
```
ansible-galaxy install -r requirements.yaml 
ansible-galaxy collection install community.general
ansible-galaxy collection install ansible.posix
```

# Set permissions on .ssh/
```
sudo chmod 700 .ssh
sudo chmod 600 .ssh/ansibleuser
sudo chmod 644 .ssh/ansibleuser.pub
```