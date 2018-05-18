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
pm2 start app.js
```

### updating node

```
cd lwf-node
```
```
pm2 stop app.js
```
```
./lwf_manager.bash rebuild

```
### When rebuilding and syncing is done

```
forever stop app.js
```
```
pm2 start app.js
```

### To check / Monitor

```
pm2 monit
```
```
pm2 monitor
```
```
pm2 status
```

