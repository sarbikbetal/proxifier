# Proxifer
A simple cli utility to set bash, env, apt, npm, git and gsettings proxy.

## Usage 
Edit the script and change the `route` and `port` variables to your desired values.
Keep this file in a safe directory and create a symlink to `/usr/local/bin/` and change it's permission to be executable 
```
$ sudo ln -s proxifier /usr/local/bin/proxifier
$ sudo chmod a+x /usr/local/bin/proxifier
```
```
$ sudo proxifier [OPTION]

-s,  --set      set-up the proxy
-u,  --unset    unset the proxy
-c,  --current  shows the currently set proxy settings
-h,  --help     show this help menu
```

With no OPTIONS it assumes `proxifier --current` 

## Example
Executing ` $ sudo proxifier -c `
gives output like this:
```
git proxy set to: http://10.30.0.1:8080
    
npm proxy set to: http://10.30.0.1:8080/
    
apt proxy set to: Acquire::http::Proxy "http://10.30.0.1:8080";
Acquire::https::Proxy "https://10.30.0.1:8080";
    
gsettings proxy set to: 'manual'
'10.30.0.1':8080
```
