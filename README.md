# VScode-basic-setting
## **架設C/C#環境以及VScode套件設定**

## **安裝Mingw**  
1. 前往 [MINGW](https://zh-tw.osdn.net/projects/mingw/releases/68260) 選擇 mingw-get-setup.exe
  ![MINGW](https://user-images.githubusercontent.com/103346268/162606829-fb8acfa6-025c-44c3-bd5e-37de224e694e.png)
  
2. 下在後點開一路安裝  
  ![image](https://user-images.githubusercontent.com/103346268/162607655-72c860b8-c4ab-418f-9c61-38688a508b69.png)  
  **這邊位置要記一下，後面要用**  
  ![image](https://user-images.githubusercontent.com/103346268/162607661-68941830-5f4a-4bb5-ac89-c930147a9691.png)  
  
3. 安裝完後會啟動 MinGW Installer Manager，找到 mingw32-gcc-g+±bin 點取左方窗格，選擇 Mark for Installation  
![image](https://user-images.githubusercontent.com/103346268/162608092-c22530d6-0f23-42d7-b1bc-ab1eaadb8731.png)

3. 選左側 All Packages，找到 mingw32-gdb-bin 點取左方窗格，選擇 Mark for Installation  
![image](https://user-images.githubusercontent.com/103346268/162608115-65be06fb-6291-4108-bd45-f92ba550a5d9.png)

4. 選擇 Installation --> Apply Change  
![image](https://user-images.githubusercontent.com/103346268/162608137-4f257a73-6497-4a8e-88e3-c9f61a650f54.png)

5. 點選Apply  
![image](https://user-images.githubusercontent.com/103346268/162608176-a6b5b120-9fed-4c83-9440-69a793d0817a.png)

3. 前往本機->右鍵->內容->進階系統設定  
  ![image](https://user-images.githubusercontent.com/103346268/162607480-3f6988bc-45a0-4dda-8ac4-c5e7cba79f4d.png)
  
4. 環境變數->系統變數->PATH->編輯->新增  
  ![image](https://user-images.githubusercontent.com/103346268/162607580-47f3502f-a514-40db-83a2-b4955fbac5c0.png)
  
4. 新增 C:\MinGW\bin 點選確定  
![image](https://user-images.githubusercontent.com/103346268/162608316-5afa5728-8602-47af-9e97-5f024877fbbf.png)


## **VScode安裝及套件設定**  
1. 前往 https://code.visualstudio.com/Download 選擇自己的平台  
  ![image](https://user-images.githubusercontent.com/103346268/162607356-7691ca69-455c-40b9-a0b1-1156f1194c72.png)

2. 打開VScode安裝延伸套件(C/c++,Code Runner)  
![螢幕擷取畫面 2022-04-10 160254](https://user-images.githubusercontent.com/103346268/162608808-8ea7590f-5c86-4365-8492-64fe9caadf46.png)
![image](https://user-images.githubusercontent.com/103346268/162607408-9c963b86-5ea0-40da-9ddd-4d1acf3b3ef1.png)![image](https://user-images.githubusercontent.com/103346268/162607426-e3120920-051f-40b3-9214-fc9b8f390ef0.png)

3. 更改Code Runner設定  
    i. 點選Code Rnner
![image](https://user-images.githubusercontent.com/103346268/162608530-3dc370a9-7f14-4d91-a545-87fad0f30836.png)  
    ii. 設定(齒輪圖案)->擴充設定
 ![image](https://user-images.githubusercontent.com/103346268/162608904-b9f2b085-3419-47d3-8a8a-2bdc6a8c1713.png)

    iii. 找到ExecutorMap->點下方 在settings.jason內編輯
![image](https://user-images.githubusercontent.com/103346268/162608970-5190321f-ed9e-4314-9ad1-e07cb1dfcee5.png)

    iiii. 找到 "code-runner.executorMap"  
![image](https://user-images.githubusercontent.com/103346268/162609817-43462ce6-d46d-4b2f-88fd-1c832b4060fe.png)

    iv. 將"cpp"後內容刪掉改為
```
 "cpp": "cd $dir && g++ -std=c++14 *.cpp  -o $fileNameWithoutExt && $dir$fileNameWithoutExt",
```
