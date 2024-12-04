##### Train Data、中央氣象局資料、Test Data 說明：

- Train Data 被分別放在 ./Additional_Traindata、./Traindata folder 底下
- 中央氣象局資料放在 ./Gov_data folder 底下
- 用來預測答案的 Test Data 是 upload.csv
- **請確保以上的資料都在 test.ipynb 的目錄底下**

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
