### Recommended to activate a Virtual Environment

python3 -m venv .venv
. .venv/bin/activate

### Check if venv is active:

### Install pip

python -m pip install --upgrade pip

### Deal with Requirements

pipreqs .

### Install all needed req

pip install -r requirements.txt

### Check for version of module (linux / Win)

- pip freeze | grep streamlit
- pip freeze | findstr streamlit

### Upgrade module

Pip install —-upgrade streamlit

### Upgrade all

pip install -r requirements.txt --upgrade

### Exit venv

deactivate
