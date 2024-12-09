## Steps 1-4 needed to start a project
### 1. Recommended to activate a Virtual Environment

```
python3 -m venv .venv
. .venv/bin/activate
```

### 2. Check if venv is active:
`which python`

### 3. Install pip

`python -m pip install --upgrade pip`


### 4. Install all needed req

`pip install -r requirements.txt`

---

### Deal with Requirements

`pipreqs .`

### Check for version of module (linux / Win)

```
pip freeze | grep streamlit
pip freeze | findstr streamlit
```

### Upgrade module

`Pip install —-upgrade streamlit`

### Upgrade all

`pip install -r requirements.txt --upgrade`

### Exit venv

`deactivate`
