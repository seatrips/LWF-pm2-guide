# lwf-use-pm2
switch to pm2 usage for lwf

### Steps to take

login to server

```
cd lwf-node
```
```
forever stopall
```
```
sudo npm install -g pm2
```
```
pm2 startup
```
```
pm2 logrotate
```
```
pm2 set pm2-logrotate:max_size 100M
```
```

