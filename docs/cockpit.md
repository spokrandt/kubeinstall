# COCKPIT


* Follow the [Install](https://cockpit-project.org/running.html#ubuntu) instruction provided by package
* add host config


# Master config
```
spokra@master:/etc/cockpit/machines.d$ cat 99-webui.json                                                                                                                      
{                                                                                                                                                                             
  "master" : {                                                                                                                                                                
    "visible" : false,                                                                                                                                                        
    "color" : "rgb(255, 190, 0)",                                                                                                                                             
    "address" : "master"                                                                                                                                                      
  }                                                                                                                                                                           
}spokra@master:/etc/cockpit/machines.d$ cat machines.json                                                                                                                     
{                                                                                                                                                                             
        "slave01": {                                                                                                                                                          
        "address": "slave01",                                                                                                                                                 
        "visible": true,                                                                                                                                                      
        "color": "red",                                                                                                                                                       
        "user": "spokra"                                                                                                                                                      
    },                                                                                                                                                                        
        "slave02": {                                                                                                                                                          
        "address": "slave02",                                                                                                                                                 
        "visible": true,                                                                                                                                                      
        "color": "green",                                                                                                                                                     
        "user": "spokra"                                                                                                                                                      
    },                                                                                                                                                                        
        "slave03": {                                                                                                                                                          
        "address": "slave03",                                                                                                                                                 
        "visible": true,                                                                                                                                                      
        "color": "yellow",                                                                                                                                                    
        "user": "spokra"                                                                                                                                                      
    }                                                                                                                                                                         
}                              
```

# Slave01 config
```
spokra@slave01:~$ cat /etc/cockpit/machines.d/machines.json                                                                                                                   
{                                                                                                                                                                             
    "master": {                                                                                                                                                               
        "address": "master",                                                                                                                                                  
        "visible": true,                                                                                                                                                      
        "color": "green",                                                                                                                                                     
        "user": "spokra"                                                                                                                                                      
    },                                                                                                                                                                        
        "slave02": {                                                                                                                                                          
        "address": "slave02",                                                                                                                                                 
        "visible": true,                                                                                                                                                      
        "color": "red",                                                                                                                                                       
        "user": "spokra"                                                                                                                                                      
    },                                                                                                                                                                        
        "slave03": {                                                                                                                                                          
        "address": "slave03",                                                                                                                                                 
        "visible": true,                                                                                                                                                      
        "color": "yellow",                                                                                                                                                    
        "user": "spokra"                                                                                                                                                      
    }                                                                                                                                                                         
}  
```
# slave02 config
```
spokra@slave02:~$ cat /etc/cockpit/machines.d/machines.json                                                                                                                   
{                                                                                                                                                                             
    "master": {                                                                                                                                                               
        "address": "master",                                                                                                                                                  
        "visible": true,                                                                                                                                                      
        "color": "green",                                                                                                                                                     
        "user": "spokra"                                                                                                                                                      
    },                                                                                                                                                                        
        "slave01": {                                                                                                                                                          
        "address": "slave01",                                                                                                                                                 
        "visible": true,                                                                                                                                                      
        "color": "red",                                                                                                                                                       
        "user": "spokra"                                                                                                                                                      
    },                                                                                                                                                                        
        "slave03": {                                                                                                                                                          
        "address": "slave03",                                                                                                                                                 
        "visible": true,                                                                                                                                                      
        "color": "yellow",                                                                                                                                                    
        "user": "spokra"                                                                                                                                                      
    }                                                                                                                                                                         
}            
```
# slave03 config
```
{                                                                                                                                                                             
    "master": {                                                                                                                                                               
        "address": "master",                                                                                                                                                  
        "visible": true,                                                                                                                                                      
        "color": "green",                                                                                                                                                     
        "user": "spokra"                                                                                                                                                      
    },                                                                                                                                                                        
        "slave01": {                                                                                                                                                          
        "address": "slave01",                                                                                                                                                 
        "visible": true,                                                                                                                                                      
        "color": "red",                                                                                                                                                       
        "user": "spokra"                                                                                                                                                      
    },                                                                                                                                                                        
        "slave02": {                                                                                                                                                          
        "address": "slave02",                                                                                                                                                 
        "visible": true,                                                                                                                                                      
        "color": "yellow",                                                                                                                                                    
        "user": "spokra"                                                                                                                                                      
    }                                                                                                                                                                         
}          
```
