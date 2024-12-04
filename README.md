##### Train Data、中央氣象局資料、Test Data 說明：

- Train Data 被分別放在 ./Additional_Traindata、./Traindata folder 底下
- 中央氣象局資料放在 ./Gov_data folder 底下
- 用來預測答案的 Test Data 是 upload.csv
- **請確保以上的資料都在 test.ipynb 的目錄底下**

##### 其餘 files 說明：

- answer.csv 為預測結果
- test.ipynb 為執行的程式碼

##### 環境說明：

- 作業系統：Windows 11 家用版 23H2
- Python : 3.12.7
- Jupter 套件：IPython(8.27.0)、ipykernel(6.29.5)、ipywidgets(8.1.2)、jupyter_client(8.6.0)、jupyter_core(5.7.2)、jupyter_server(2.14.1)、jupyterlab(4.2.5)、nbclient(0.8.0)、nbconvert(7.16.4)、nbformat(5.10.4)、notebook(7.2.2)、qtconsole(5.6.0)、traitlets(5.14.3)
- 相關 import 套件：numpy(1.26.4)、matplotlib(3.9.2)、seaborn(0.13.2)、pandas(2.2.3)、scikit-learn(1.5.2)、xgboost(2.1.2)、scipy(1.14.1)

##### Block 執行方式：

- Block 第一行會有一行註解
  - **(O)** 代表分析圖表的 code，可以依照需求做使用
  - **(X)** 代表測試 code，用於報告分析，**請勿使用**。
  - **(i)** i 若為數值(ex. 1、2、3...)，則代表執行的順序

##### 分析圖表的使用方式：

- 有三個分析圖表的 Block
  - 前面兩個通常是在輸出 Sunlight Histogram 的直方圖
  - 最後一個是用於輸出 Sunlight(Lux)與 Power(mW)的分布圖
    - 最前面有一行 **train_data = tmp_data.copy()**，可以通過更改後面的變數查看階段的情況
      - **tmp_data**為最原始的 train data
      - **data1**為 LocationCode 1、2、5、7 修正完 Sunlight(Lux)異常值(54612.5)的 data
      - **data2**為 LocationCode 1、2、5、7 修正完異常值，並且重建了 max_Sunlight(117758.2)的資料
      - **data3**為利用先前已修復完的 LocationCode 1、2、5、7 的資料，對其餘 LocationCode 進行重建後所得的資料
