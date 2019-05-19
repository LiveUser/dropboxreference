# Dropbox v2 API Unofficial Docs

#### By Radamés J. Valentín Reyes

### API Setup

- Create a dropbox account
- Create an app on https://www.dropbox.com/developers 
- Generate a token
- on your node.js project folder run "npm install dropbox" or "sudo npm install dropbox" on linux
- now run "npm install isomorphic-fetch"

```javascript
var fetch = require('isomorphic-fetch');
var Dropbox = require('dropbox').Dropbox;
const dbx= new Dropbox({
    accessToken: 'yourAccessTokenHere',
    fetch:fetch,
    });
```



--------------------------------------------------------------

### Upload File

```javascript
dbx.filesUpload({path: '/yourPathHere', contents: yourFileContents})
          .then(function(response) {
            console.log(response);
          })
          .catch(function(error) {
            console.error(error);
          });
```



------------------------------------------------------

### Delete File

```javascript
dbx.filesDelete({path: '/yourPathHere'}).then(()=>{
                    
                }).catch((error)=>{
                    console.log(error);
                });
```



-------------------------------------------------

### Get folder contents

```javascript
dbx.filesListFolder()
        .then(function(response) {
          console.log(response);
        })
        .catch(function(error) {
          console.error(error);
        });
```



----------------------------------------------------------------

### Download File

```javascript
dbx.filesDownload({path: '/yourPathHere'})
        .then(function(data) {
            console.log(data.fileBinary);
        })
        .catch(function(error) {
          console.error(error);
        });
```

--------------------------------------------------

### Get All Folder Contents

```javascript

```

