## 更新紀錄
  * 07/03/2015 新版2015音源的日語區完全完成
  * 06/05/2015 從sourceforge搬遷到github
  * 01/??/2015開始2015更新計劃
  * 01/15/2013更新，上傳20140115版

## 目標
  * 本計畫是作能唱華語（台灣風格）與日語的虛擬歌手，徵音梅林。
  * Purpose of the project is to make a virtual singer "Linne" which can sing Mardarin(Taiwanese accent) and Japanese.
  *Pronunciation :Mandarlin- 徵(Zhi)音(Yin)梅(Mei)林(Lin) , Japanese- 徴（ち）音（おん）梅（メイ）林（リン）

## 檔案說明
  * tar.gz請用  " tar xvf 檔名 " 解開（其他平台請使用可以用的解壓縮軟體來解）
  * wav目錄裡面的聲波檔是錄音原始檔（24bit 48000hz mono）都是無損壓縮的flac，Unix系平台使用者，在解開的目錄下，複製貼上執行下面這一行，就可以還原成原來的wav檔
(The wav files in wav folder are the original source recorded in professional studio. Sample files are 24bit 48000hz mono.)

```sh
for i in *.flac ; do flac -d $i ; done;rm *.flac
```
發佈版的包裝檔則是已經後製過（去抵噪、消脣齒音等 ）的16bit 44100hz mono的聲波取樣，能給UTAU或LINNE平台來使用的。
The publish version is filled with  16 bit 44100hz mono wave sample files. Can be read by  UTAU or Linne platform.  * Voicebank is filled with  16 bit 44100hz mono wave sample files. Used by EFB-GW.

## wav檔案下載
  * 從github clone `git clone https://github.com/ProjectMeilin/meilin-voicebank.git`

## csv
 * 所有錄音的列表。**output.csv**是```華語```的，**output_japanese.csv**是```日語```的，others是其他項目或者將來增補的。檔案內的項目格式是：
 * 該語文方便人看的音標（注音或者假名）,IPA標示,檔名
 * 第一項是為了方便一般人閱讀，其中由於音標有時並不能真實記載實際的語音的變體，例如「**ㄇㄛ**」這個單獨音，「**麼**」跟「**魔**」注音一模一樣，但是實際發音不同，記載上，我們會加上大寫英文的後綴來編碼表示，標示為A的，會選擇日常生活最常用的那一個。
 * IPA標示則是程式運算的邏輯
 * 檔名是為了跨系統平台，各種編碼系統可以正確顯示而設定，所以編成ASCII，編輯的邏輯使用語言標音的羅馬拼音。
 * 華語首字使用小寫，日語使用首字使用大寫
