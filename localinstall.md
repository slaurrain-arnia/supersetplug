# Local install

[text](https://medium.com/@nandwalritik/apache-superset-local-installation-7958cbf7c5f4)

need node version > 18 (wtf ?)

wget https://nodejs.org/dist/v20.17.0/node-v20.17.0-linux-x64.tar.xz
sudo tar -xJf "node-v20.17.0-linux-x64.tar.xz" -C /usr/local --strip-components=1 --no-same-owner
rm node-v20.17.0-linux-x64.tar.xz


### Clone the Apache Superset Repository

git clone https://github.com/apache/superset/
cd superset

### Front-End Setup

cd superset-frontend
npm ci
npm run build

This will be build the front assets necessary to run the UI for superset.
(
    NOTE : If you are making any changes to frontend codebase and want to see the changes in hot-reload mode, run it using following command and open superset on localhost:9000.

npm run dev-server)


### Backend Setup

Create a virtual environment with following command

python3 -m venv supersetDev
source ./supersetDev/bin/activate

Install the external dependencies and install superset in development mode

(under root of superset)
pip install -r requirements/base.txt
do not work : pip install -r requirements/development.txt

pip install -e .

## Set secret key

export SUPERSET_SECRET_KEY='y%+DDg#+2N3Cc+w/Ktg:RPKJ>RXBC%D(dM3_U,5u:KSD9?;DmNUDchYDWB;Uy?T9'

## After above installation we need to initialize the database.

superset db upgrade

##  Create superset Admin User

Note down the credentials you will input after below command, because that will be the login credentials for Superset Admin User.

superset fab create-admin

## Creating default roles and permissions

superset init

## Load some sample data to play with

superset load-examples

## Starting Superset Server

superset run -p 8080 --with-threads --reload

Now you can open superset in browser on localhost:8080 

