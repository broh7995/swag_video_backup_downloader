# swag_video_backup_downloader
#### Windows application for download videos from https://app.swag.live/

## Step 1:
  Download application from [Here](https://drive.google.com/file/d/1xWCf1ZJtc-jfDjYwK0GNg76VZWRRvd0E/view?usp=sharing).

## Step 2:
  Open browser and navigate to https://app.swag.live/ and login your account.
  
## Step 3:
  To extract token press F12 to open DevTool from your browser and paste the code into the console.
  ```
  var db;
  var request = indexedDB.open("localforage", 2);
  request.onsuccess = function() {
    db = request.result;
    var tx = db.transaction("keyvaluepairs", "readonly");
    var store = tx.objectStore("keyvaluepairs");
    var _request = store.getAll("_accessToken")
    _request.onsuccess = function() {
      var token = _request.result.toString();
      console.log(token);
    };
  };
  ```
  
## Step 4:
  Copy and paste your token into `token.txt` then save and close it.
    
## Step 5:
  Double click to run the application `swag_backup_downloader.exe` then if your token is vaild the download will begin shortly.
