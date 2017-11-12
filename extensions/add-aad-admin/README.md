# add-aad-admin Extension

Adds a role binding constraint for the given object.


You can validate that the extension was run by running (make sure you have tunneled into the master):
```
ls -l /var/log
```

# Configuration
|Name|Required|Acceptable Value|
|---|---|---|
|name|yes|hadd-aad-admin|
|version|yes|v1|
|extensionParameters|yes user or group object||
|rootURL|optional||
|script|required|add-aad-admin.sh|

# Example
``` javascript
    "masterProfile": {
      ...
      "extensions": [
        { 
          "name": "aad-default-admin", 
          "singleOrAll": "single"
        }
     ]
    },
    ...
    "extensionProfiles": [
      { 
        "name": "aad-default-admin", 
        "version": "v1", 
        "script": "add-aad-admin.sh" 
        "extensionsParameters": "https://sts.windows.net/e2917176-1632-47a0-ad18-671d485757a3/#22fa281b-bf62-4b14-972c-0dbca24a25a2"
      }
    ]
    

```

# Supported Orchestrators
All