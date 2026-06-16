好的，這是我幫你重新整理、精簡且格式完全統一的完整版 README.md 內容。
這個版本已經將你的主資料夾與 outputs/ 目錄結構、11,946 筆有效樣本數、以及剛剛精煉過、不臃腫的研究問題全部完美整合。中英文雙語對照的排版非常專業，你可以直接整段複製到你的 GitHub 專案主頁：
📊 YRBSS 青少年生活行為與睡眠時間之複線性迴歸分析 / Predictors of Adolescent Sleep Duration: A Multiple Linear Regression Analysis
👥 團隊資訊 / Group Information
組別 / Group Number: Individual Project
學生姓名 / Name: 謝函芸
學號 / Student ID: (請在此填入你的學號)
💾 使用數據 / Dataset
數據集名稱 / Dataset Name: 2007 Youth Risk Behavior Surveillance System (YRBSS) / 2007 年青少年危險行為調查
來源 / Source: Centers for Disease Control and Prevention (CDC) / 美國疾病管制與預防中心
有效樣本數 / No. Observations: 11,946 筆
🔍 選定變數與資料清洗 / Selected Variables & Data Cleaning
根據我們的 Python 資料清洗邏輯，我們從原始 YRBSS 數據中篩選出一個核心依變數與三個二分（Binary）自變數，用以探討青少年生活行為： According to our Python data cleaning logic, we selected one core dependent variable and three binary independent variables from the YRBSS dataset to explore adolescent lifestyle behaviors:
依變數：睡眠時數 / Dependent Variable: Sleep Duration (Sleep)
定義: 青少年每晚的平均睡眠時數（連續型變數，範圍 4 至 10 小時）。

自變數一：大麻初次使用年齡 / Independent Variable 1: Marijuana Initiation (InitiationOfMarijuaUse)
1: 曾在青少年早期或之前嘗試、使用過大麻（風險行為群體）。
0: 從未嘗試或使用過大麻（對照群體）。
自變數二：固定水果攝取 / Independent Variable 2: Regular Fruit Eating (FruitEating)
1: 平常有規律攝取水果的健康飲食習慣（健康行為群體）。
0: 沒有規律攝取水果（對照群體）。
自變數三：每日看電視習慣 / Independent Variable 3: Daily Television Watching (TelevisionWatching)
1: 每日固定花費時間觀看電視（靜態生活行為群體）。
0: 每日無固定看電視習慣（對照群體）。
📊 統計檢定方法 / Statistical Methodology
我們採用 複線性迴歸分析 (Multiple Linear Regression, OLS) 進行推論統計。此方法能在「同時控制其他混淆變數」的條件下，估計各個獨立行為對青少年睡眠時間的淨效果（Net Effect），並計算 95% 信賴區間（Confidence Intervals）以檢驗統計顯著性。
模型公式如下 / Model Formula:
Sleep=β 
0
​	
 +β 
1
​	
 (InitiationOfMarijuaUse)+β 
2
​	
 (FruitEating)+β 
3
​	
 (TelevisionWatching)+ϵ
❓ 研究問題 / Project Questions
總體研究問題 / Overall Research Question:
中文：本研究旨在探討藥物濫用（大麻使用）、健康飲食（水果攝取）及靜態娛樂（觀看電視）個別對青少年睡眠時數的獨立影響與反應。
English: This project investigates the individual impacts of substance abuse (marijuana use), healthy diet (fruit consumption), and sedentary entertainment (television watching) on adolescent sleep duration.
具體子問題與統計假設 / Specific Questions & Hypotheses:
📌 1. 藥物濫用對睡眠的影響 / Impact of Substance Abuse (β 
1
​	
 )
中文：初次嘗試大麻的風險行為，是否與較短的青少年睡眠時數具有顯著相關？
English: Is early marijuana initiation significantly associated with reduced sleep duration among adolescents?
Hypothesis: H 
0
​	
 :β 
1
​	
 =0vsH 
1
​	
 :β 
1
​	
 

=0
📌 2. 健康飲食對睡眠的影響 / Impact of Healthy Diet (β 
2
​	
 )
中文：規律攝取水果的健康飲食習慣，是否對青少年睡眠時數帶來正向反應？
English: Does maintaining a regular fruit-eating habit predict a positive response in adolescent sleep duration?
Hypothesis: H 
0
​	
 :β 
2
​	
 =0vsH 
1
​	
 :β 
2
​	
 

=0
📌 3. 觀看電視對睡眠的影響 / Impact of Television Watching (β 
3
​	
 )
中文：每日觀看電視的娛樂行為，在控制其他因素後對青少年睡眠時數的淨影響為何？
English: What is the net effect of daily television watching on adolescent sleep duration after controlling for other behavioral factors?
Hypothesis: H 
0
​	
 :β 
3
​	
 =0vsH 
1
​	
 :β 
3
​	
 

=0
