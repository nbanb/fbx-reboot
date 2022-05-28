# fbx-reboot
Very simple tool to reboot your Freebox (using API library: fbx-delta-nba_bash_api.sh)
#### To be run on Freebox hardware from FREE (French Internet Provider)



--------------------------------------------------------------------------------------------------------------------
### README of fbx-reboot program
--------------------------------------------------------------------------------------------------------------------



sourcing lib : `fbx-delta-nba_bash_api.sh`

You can get the library here on this branch (at the time I'm writing, changes are not merged on the original project, so use the branch):
https://github.com/nbanb/fbx-delta-nba_bash_api.sh/tree/nbanb-freebox-api

You need to have `curl` and `openssl` installed.

Get the source:

    $ curl -L https://github.com/nbanb/fbx-delta-nba_bash_api.sh/raw/nbanb-freebox-api/fbx-delta-nba_bash_api.sh > fbx-delta-nba_bash_api.sh


First get a token which allow this app to login Feebox Delta API :

#### *  authorize_application *app_id* *app_name* *app_version* *device_name*
It is used to obtain a token to identify a new application (need to be done only once)
##### Example
```bash
$ source ./fbx-delta-nba_bash_api.sh
$ authorize_application  'MyWonderfull.app'  'My Wonderfull App'  '1.0.0'  'Deb 11'
Please grant/deny access to the app on the Freebox LCD...
Authorization granted

MY_APP_ID="MyWonderfull.app"
MY_APP_TOKEN="4uZTLMMwSyiPB42tSCWLpSSZbXIYi+d+F32tVMx2j1p8oSUUk4Awr/OMZne4RRlY"
```


#### Now you can download & update fbx-reboot with your just obtained values.

```bash
$ curl -L https://raw.githubusercontent.com/nbanb/fbx-reboot/main/fbx-reboot >fbx-reboot 
$ chmod +x fbx-reboot
```

Update `fbx-reboot` program with your just obtain values :
```bash
MY_APP_ID="YourNewFBXVM.app" 
MY_APP_TOKEN="YourNewFBXVM.app.JustObtainToken"
```

#### That's all, now you are ready to use this tool which reboot your Freebox from your bash session

