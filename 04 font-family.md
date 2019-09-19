## 五大字戰隊（font-family）

★ 村外西南方小樹林 ↓↓↓

**顯示樹林位置圖**

*也不知道村長什麼意思？
邊走邊打開手上紙條，
上面寫著*：

（疑～）字體與字型使用區別：

- 字體：泛指不同家族，明體、黑體和書寫字體等。
- 字型：思源宋體、新細明體和 Helvetica 等電腦用字。

：前方有人？
瞬間！ )


Σ(lliдﾟﾉ)ﾉ：
*你 你們到底是誰？*

：既然你誠心誠意的發問了，

：我們就大發慈悲的告訴你，

：為了防止「inline」世界被破壞，

：為了守護排印世界的和平～～

等等！！！
*你這擺明抄襲某～～*

：小子，我們就是傳說中，

完全被忽視 XD )

![基紐特戰隊](https://www.itsfun.com.tw/images/eb/42/nBnauUTMmhTZlFzM2cjNlVDN3UTMwQ3Lt92Yuc2cthWcuw2cz5SMw9yL6MHc0RHa.jpg)

( 註 圖片來源：[七龍珠 基紐特戰隊](https://zh.wikipedia.org/wiki/%E4%B8%83%E9%BE%8D%E7%8F%A0_(%E5%8B%95%E7%95%AB)) )

---

★★★ 關卡條件 ↓↓↓

### 五大字戰隊（font-family）

**serif**：襯線字體 (明體)。筆劃結尾有特殊的裝飾線或襯線，(喇叭形或錐形末端)，字體通常按比例間隔。在粗筆劃和細筆劃之間顯示更大的差異，較無襯線字體更適用於長篇小說內文。

如 Mincho (日語)，Sung 或 Song (中文)，Batang (韓語-明朝體) 或 Naskh (阿拉伯語) 風格任何如此描述的字體都可用於表示通用的 serif 系列。

![樣本襯線字體](https://drafts.csswg.org/css-fonts-3/serifexamples.png)

---

**sans-serif**：無襯線字體 (黑體)。通常是低對比度 (垂直和水平筆劃具有接近相同的厚度)，並且具有平滑的筆劃結尾，沒有任何擴口，交叉筆劃或其他裝飾，字體通常按比例間隔。常常給人機械、幾何的清淨感，有時夾帶些許人文氣息，並可提高辨識的功能性。

如 Gothic (日語)，Hei (中文)或 Gulim (韓語-歌德體)。如此描述的任何字體都可用於表示通用的 sans-serif 系列。

![樣本sans-serif字體](https://drafts.csswg.org/css-fonts-3/sansserifexamples.png)

註：無襯線體約為 19 世紀末葉發明，名稱原指 grotesque 很怪的東西。現有許多形態 (粗細對比較高、疑似帶有襯線)，詳細可參考 [justfont blog ( sans-serif 篇 ) ](https://blog.justfont.com/2014/06/google-fonts-2/#more-5861)。

---

**monospace**：等寬字體 (mono 為單一意思)。泛指字元寬度相同的定寬字體 (fixed width)。按等寬間隔，是所有字元具有相同的固定寬度。現有程式碼以及文字介面的程式，如虛擬終端機等也經常使用，除了排列整齊，字母之間形狀差異明顯，極適合 debug。

![樣本等寬字體](https://drafts.csswg.org/css-fonts-3/monospaceexamples.png)

---

**cursive**：書寫字體。通常使用更加非正式的文本樣式，更像是手寫筆或筆刷而不是印刷字母 (別名如 Chancery，Brush，Swing 和 Script)。其中一些字符以流動的方式書寫在一起，是為了使書寫更快。隨意的草書是連接和筆式升降機的組合，書寫風格進一步又分為「循環」，「斜體」或「連接」。

![樣本草書字體](https://i.imgur.com/oOa8iLJ.png)

---

**fantasy**：幻想字體主要是裝飾性或表達性字體，包含字符的裝飾或表現形式。瞥除不代表實際字符的 Pi(π) 等。

![樣本幻想字體](https://drafts.csswg.org/css-fonts-3/fantasyexamples.png)

**迷之角色 [字戰隊]**：
看完~~盜版基紐特戰隊登場後~~，
*有了以上基本認知*（我的感受？！）

：回到剛～～

╮(╯_╰)╭ 
已放棄抵抗。)

---

#### [字體家族屬性](https://drafts.csswg.org/css-fonts-3/#font-family-prop) 可區分如下：

- **字型家族名稱：family-name**
主字型名稱。如 `Times` 和 `Helvetica` 皆是系列之一。字型名稱如中間含括空格時，需加入前後引號 (半形)。

- **字體通用名稱：generic-name**
當指定主字型家族名稱失效時，這些通用名稱關鍵字可用作一般回退（備選）機制，給出相符合的替代字體 (無需額外添加引號)。如下方替 `<body>` 增設字型，因`Helvetica`、``'Open Sans'`` 皆為無襯線字體系列，排序最後通用字體理應設定為 `sans-serif` 以符合前方同類型設定值。

```css=
body { font-family：Helvetica, 'Open Sans', sans-serif; }
```

- 與其他 CSS 屬性不同，組件值是以**半形逗號分隔**的列表，表示**備選方案**。
- 至少選用一個字型家族名稱和一個字體通用名稱。
- CSS 選擇機制僅提供了在需要替換時，確定**最接近**替代的方法。
- 考慮字型的可用性，選擇 `Futura` 家族名稱會匹配所有，但單指定 ``'Futura Medium'`` 其他字重失效。

(|||ﾟдﾟ) 
看來不太妙 ）

偷瞄 )
往旁默默移動中。

( 沙沙～～)

**對方完全無視
繼續說著：**

★ `font-family` 屬性指定的是一個優先級從高至低的可選字型列表，字型的選定不是在發現用戶主系統上安裝的列表中的第一個字型時停止。相反，對字型的選擇是逐字進行的，也就是說即使某個字符周圍都在某個字型中可以顯示，但該字符在當前的字型文件中沒有合適，將會繼續嘗試列表中排序後方的字型直到最後列表字體為止。

★ 有效的字型家族名稱需以「字符串」形式引用，這意味著在沒有帶引號的字型家族名稱的開頭是不能使用標點符號字符和數字字符進行轉義。

★ 因無法保證用戶的主系統內已安裝了指定的字型，也不能保證使用 `@font-face` 樣式屬性提供的外聯字型是否為有效超連結情況下，如無提供通用字體，則使用瀏覽器設置的神秘的默認字體。

...
...
...

**To Be Continued ...**

---
[ 追加經驗值 ]

註：參考來源 [W3C CSS Fonts Module Level 3](https://drafts.csswg.org/css-fonts-3/#font-family-prop)

關於 MDN 由 Mozilla Contributors 製作，以 CC-BY-SA 2.5 釋出。
