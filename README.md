### Step 1 — Setting Up Python 3

https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-local-programming-environment-on-ubuntu-18-04

sudo apt update
sudo apt -y upgrade

sudo apt install -y python3-pip

sudo apt install build-essential libssl-dev libffi-dev python-dev

### Step 2 — Setting Up a Virtual Environment

sudo apt install -y python3-venv

mkdir environments
cd environments

python3 -m venv my_env

source my_env/bin/activate

### Step 3 — Installing Flask

# in virtual env
pip install flask

#to comfirm flask installation
python -c "import flask; print(flask.__version__)"
output will be '1.1.2'

### Step 4 — Creating a Base Application and run
nano hello.py

`from flask import Flask

app = Flask(__name__)


@app.route('/')
def hello():
    return 'Hello, World!'`

export FLASK_APP=hello
export FLASK_ENV=development
flask run

### Step 5 — Using HTML templates
