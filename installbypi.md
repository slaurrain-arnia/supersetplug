# Superset by pi

## gpt said

https://chatgpt.com/c/66ec2100-1b74-8004-ac50-c260b2fc9d56

apt install -y nodejs npm

python3 -m venv superset-dev-env

source superset-dev-env/bin/activate

pip install apache-superset

export FLASK_APP=superset


## 

```
export SUPERSET_SECRET_KEY='y%+DDg#+2N3Cc+w/Ktg:RPKJ>RXBC%D(dM3_U,5u:KSD9?;DmNUDchYDWB;Uy?T9'
```

(/superset/superset/superset-dev-env/lib/python3.11/site-packages/superset/config.py)


superset db upgrade

pip install pillow

cd superset-dev-env/lib/python3.11/site-packages/superset/static/assets

wget https://nodejs.org/dist/v16.20.0/node-v16.20.0-linux-x64.tar.xz
sudo tar -xJf "node-v16.20.0-linux-x64.tar.xz" -C /usr/local --strip-components=1 --no-same-owner
rm node-v16.20.0-linux-x64.tar.xz


npm install --force




## clean

rm -rf node_modules
rm package-lock.json 
npm cache clean --force

##
inside env !
(superset-dev-env) slaurrain@superdeb:~/DEV/arnia/superset/superset$
superset run -p 8088 --with-threads --reload --debugger


## load examples
superset load-examples



