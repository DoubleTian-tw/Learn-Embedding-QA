# Learn-Embedding-QA
將原本OPENAI提供的[QA範例](https://platform.openai.com/docs/tutorials/web-qa-embeddings/how-to-build-an-ai-that-can-answer-questions-about-your-website)進行調整，直接更改scraped.csv檔案後製作自己的QA機器人

## Step1
download zip或clone專案到自己的桌面

## Step2
打開scraped.csv進行修改，文字內容改成你想要的問與答(因為內容是中文所以檔案會是Big5)

## Step3
(可做可忽略)
[建置python虛擬環境](https://github.com/DoubleTian-tw/Python-env.git)
利用虛擬環境來執行專案，之後不要用了還可以刪掉

## Step4
開啟cmd進入虛擬環境(有虛擬環境才需要)

## Step5
安裝套件
```
pip install -r requirements.txt
```

## Step6
下指令，這個動作會把scraped.csv轉換成向量embeddings.csv
```
python 01_turn-to-embedding.py
```

## Step7
開始施詠唱，Do-re-mi-so!
```
python 02_answer-QA.py "你的Question"
```
如果出現I don't know的幾種可能: <br>
1.scraped內沒有相關的文字，例如csv沒有美國的美食，但是你問了這個問題  <br>
2.scraped內問了相反的文字而且字詞沒有出現，例如csv內都是牛肉麵好吃的回答，但是你問了"不"好吃  <br>

## Step8
沒意外的話這樣就完成基本的QA機器人了 <br>
之後或許可以套在Line上面會比較方便使用 <br>
有機會再更新 <br>
