# brctldriver
Nodejs Linux bridge Control(brctl) utility wrapper

Supports the following API
1. Create a Bridge              
2. Add Interface to the Bridge           
3. Enable the Bridge                
4. Disable the Bridge               
5. Delete the Bridge              
6. Get the Status of the Bridge

## API:
1. createBridge : (bridgname, callback)               
2. addInterface : (bridgname,ifname,callback)
3. enableBridge : (bridgname, callback)
4. disableBridge : (bridgname , callback)
5. deleteBridge : (bridgename, callback)
6. getStatus: (bridgename, callback)
    returns "running" or "notrunning"


## Program Example 
written in coffeescript.         
This is just indicative program to demonstrate functionality . It cannot run as it is.         


        brctl = require('brctldriver')
        brctl.createBridge "sw1", (result) =>
            util.log "Bridge creation " + result                               
        brctl.addInterface "sw1", "veth1",(result) =>
            util.log "AddInterface result", result


This driver is used in Kaanalnet application to manage linux bridge, 
https://github.com/sureshkvl/kaanalnet/blob/master/src/builder/switchCtrl.coffee

   

