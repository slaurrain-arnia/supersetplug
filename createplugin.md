# Create plugin
https://superset.apache.org/docs/contributing/howtos/

# seems to need node 16 (sic)
wget https://nodejs.org/dist/v16.20.0/node-v16.20.0-linux-x64.tar.xz
sudo tar -xJf "node-v16.20.0-linux-x64.tar.xz" -C /usr/local --strip-components=1 --no-same-owner
rm node-v16.20.0-linux-x64.tar.xz


(sudo) npm i -g yo
cd superset-frontend/packages/generator-superset
npm i
(sudo) npm link

mkdir /tmp/superset-plugin-chart-hello-world
cd /tmp/superset-plugin-chart-hello-world


## initiate plugin

