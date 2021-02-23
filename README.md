# rasa_dev_setup
Developer Environment Setup for RASA

First Create Conda Environment
```
conda create -n rasa_env python=3.8
```
Activate the env and install dependencies
```
conda activate rasa_env
conda install ujson
conda install numpy
conda install tensorflow
```
```
pip3 install rasa
```

### Hosting RASA X with ngrok
Install RASA X
```
pip3 install rasa-x --extra-index-url https://pypi.rasa.com/simple
```
If it takes too long then
```
pip install --upgrade pip==20.2
```

Install ngrok
```
wget linux_download_link
unzip ...ngrok.zip
```

[Authenticate with ngrok account](https://dashboard.ngrok.com/get-started/setup)
```
./ngrok authtoken key
```

Run
```
./ngrok http 5002
```

Export ip to RASA X
```
export RASA_X_HOSTNAME= ip from ngrok
export RASA_X_HOST=ip from ngrok
export RASA_X_PASSWORD=any
```

Run RASA X
```
rasa x
```
