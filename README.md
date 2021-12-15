# swag_video_backup_downloader
:movie_camera::movie_camera::movie_camera::movie_camera:
#### Windows application for download videos from https://app.swag.live/ 

## Step 1:
  Download application from [Here](https://drive.google.com/file/d/1PYh0H629jz3Uxpq9J3P2nLfpBNwTa4gj/view?usp=sharing)(google drive).:toolbox:

## Step 2:
  Open browser and **Navigate** to https://app.swag.live/ and **Login** your account.
  
## Step 3:
  To extract token open any page in https://app.swag.live/ and **Press F12** to open DevTool from your browser then **Paste** the following code into the console. Hit **Enter** then your token will be printed.
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
  **Copy and paste** your token into `token.txt` then save and close it.
    
## Step 5:
  **Double click** to run the application `swag_backup_downloader.exe` then if your token is vaild the download will begin shortly.:+1:
  
  
---------------

# swag 影片備份下載器
:movie_camera::movie_camera::movie_camera::movie_camera:
#### Windows的程式，用來下載在 https://app.swag.live/ 上購買的影片與圖片.

## 第一步:
  **下載**[主程式](https://drive.google.com/file/d/1PYh0H629jz3Uxpq9J3P2nLfpBNwTa4gj/view?usp=sharing)(google drive).:toolbox:

## 第二步:
  使用瀏覽器開啟網頁 https://app.swag.live/ 並且**登入**Swag帳號.
  
## 第三步:
  在 https://app.swag.live/ 的任何頁面**按下F12** 打開開發者工具把下面的程式碼複製貼上在console內按下**Enter**鍵, Token就會印在下方
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
 
  
## 第四步:
  打開`token.txt`檔案並把token複製貼上來, 存檔並關閉`token.txt`.
    
## 第五步:
  執行應用程式`swag_backup_downloader.exe`, 如果token驗證成功下載就會開始了:+1:
