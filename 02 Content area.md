## 鉄人28号FX　鉄人2号「文本士」

★ 村落裡某一角落 ↓↓↓

**顯示武器店位置圖**

**武器店前 [文本士]**：

*你是否能在預設情況下，*

*對行內元素進行設定樣式屬性 width 與 height？*

繼續接著說：

- 對於「inline」設定寬度與高度**失效是正常**。
- 而對「inline」設定寬度與高度**能正常顯示**。

**閱讀前，建議先向 [鉄人1号「行內熊」](https://ithelp.ithome.com.tw/articles/10215954)收集資料，此章為初探村落續文。**

---

★★★ 關卡條件 ↓↓↓
### 內容區域（Content area）

((ﾟдﾟ))：

*什麼區域？ 跟剛說的有關？*

*還有樣式啥屬性？*

：年輕人終究還是年輕人～～

：痾！XD 

首先從 **MDN** 官方文件理解何謂 [CSS 基礎盒模型 (Box Model)](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)：

當對一個文檔 (HTML) 進行佈局時，瀏覽器的渲染引擎會根據標準之一的 CSS 基礎盒模型 (CSS basic box model)，將所有元素表示為一個個矩形盒子 (box)。CSS 決定這些盒子的尺寸、位置以及屬性 (如顏色、背景、邊框尺寸等)。

而範圍由內容邊界限制，呈現最真實**寬與高**，如文本、圖像或為一個視頻播放器。它的尺寸為內容寬度和高度 (或稱 content-box 寬高度)，並通常含有一個背景顏色 (默認為透明色) 或背景圖像。 

![MDN盒模型](https://mdn.mozillademos.org/files/8685/boxmodel-(3).png)

每個盒子又分別由四個區域組成，其效用由它們各自的邊界 (Edge) 所定義。如圖所示，與區域相對應：內容邊界、內距邊界、邊框邊界、外距邊界，而每個邊界皆可以通過其相應的屬性獨立控制。

 ﾟ∀ﾟ)σ 
 **★ 等級提升**：莫名！ )

- 引入外聯字型時，無法透過 CSS 屬性對字型寬高原始值做任何設定。
- 經 CSS 盒模型確認該內容如何正確渲染，寬高度形成，最終以文本自身決定。

>行高 (line-height)、內距 (padding) 和外距 (margin)，看似可改變其顯示範圍，但實際上皆無法直接對 content-box 進行設定。

**道具屋旁 [文本士]**：
*既然內容範圍皆由文本決定，

以下更進一步分別從不同視角去理解何謂字型預設值。*

：又是你？

整個村落都是你的咖啡館？

*：臭小子，給我~~泡杯~~不是*

：放尊重點！！

**字體概述（typography）** 首先參考繪製圖，如下：

![justfont](https://blog.justfont.com/wp-content/uploads/2013/01/typography.jpg)
（註 圖片來源：[英文 UI 字型大評比：視認性測試](https://blog.justfont.com/2013/01/ui-font-testing-legibilit/) )

- em：字型排印學的計量單位，最初表示的是字型中大寫 M 的寬度及所用的相對單位。
- 中央線 (mean line)：c、n、x、z 等小寫字母的頂端線，從基準線至中央線之間高度，稱為 x-height (ex)。
- 上端線 (ascender line)：中央線到上端線之間高度，也就是 b、f、k 等字母上面凸出段。
- 下端線 (descender line)：g、j、p 等字母，超過基準線下方的部分。
- cap line：大寫高度的頂端。基準線到 cap line 之間的高度稱為 cap height。許多字型設計上會另外安排一條大寫的頂端線，例如可稍微區分大寫 I 與小寫 l 的高度，而通常又比小寫字母最頂端稍降。

---

*續著看其他字體軟體設定*：

![image alt](https://www.high-logic.com/fontcreator/manual11/fontcreator_039_font_settings_metrics.png)

（註 圖片來源：[High-Logic 字體軟件公司](https://www.high-logic.com/) )

x 高度、m 寬度和 n 寬度等皆是字型相關長度度量，而其中又包含行間隙 (line gap)，種種設定皆對字型產生直接影響，說明了引入不同字型時，已直接包含各種自身預設值，經由瀏覽器直接渲染。

一般來說：ascender、descender 的高度差異不會太大，否則 b、p 看起來就會很不對稱。另外，請稍加注意一下在討論 TrueType、OpenType 字型技術的術語上，通常把基準線到上端線之間的整個高度稱之為 ascent。與傳統 ascender 的定義不太相同。

ヽ(✿ﾟ▽ﾟ)ノ!

**★ 拔取藥草一株**

透過游標反選，或許可觀察顯示其預設範圍。但字級尺寸設定為 30px，高度卻顯示 42px？

![Content area](https://i.imgur.com/OFxdFsY.jpg)


(\*´д\`) 

突然想認真了起來：

*既然對於「inline」設定寬度與高度失效是正常，*

*為何你又說：「inline」設定寬度與高度能正常顯示？*


**Siri 口吻 [文本士]**：

*有什麼我可以幫忙的嗎？* 

**To Be Continued ...**

[ 追加經驗值 ]

註：參考來源 [MIT - Typography ](http://web.mit.edu/6.813/www/sp18/classes/16-typography/)

[ [ But桑專欄 ] 字型設計自己來](https://blog.justfont.com/2012/11/latin-type-design-1/)

[W3C Box model](https://www.w3.org/TR/CSS22/box.html)
