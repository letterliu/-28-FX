## 鉄人28号FX　鉄人1号「行內熊」

>謎之音：
網路世界 95％ 的訊息皆是圖文。
可以合理地說，前端設計師應該在塑造文本訊息的主要學科中獲得良好的培訓，
也就是現今的排印學。—— *Oliver Reichenstein*

而「**圖像**」與「**文本**」布局整合，又同來自一個共同點： **inline** 元素。

★ 地圖東南方林中村落 ↓↓↓

**顯示村落位置圖**

**村長**：
*去去！別一直在我面前閒晃！*

*先在村裡，*

*到處收集相關資料吧。*

★★★ 關卡條件 ↓↓↓

### 行內元素（inline element）

>In an [Inline formatting contexts](https://www.w3.org/TR/CSS2/visuren.html#inline-formatting), boxes are laid out horizontally, one after the other, beginning at the top of a containing block.

村長家門外紙貼著，

：*疑！好像公告些什麼！？*

一般情況下：

內容：只能包含資料或和其他行內元素共排列。
格式：不會直接重頭在新行上開始，只佔用限定的寬度，呈現不間斷的續排文檔流。

- 行內元素以不同的方式垂直對齊 (vertical-align)，或者遵從預設文字基線 (baseline) 對齊排序。
- 形成一行的隱形矩形區域稱為線框 (line-box)。線框的寬度由塊框元素 (block) 和浮動元素 (float) 確定。
- 線框的高度由行高 (line-height) 計算部分中給出明確規則。

**NPC [行內熊]**：

*HTML 標籤裡的所有文本內容，實際上都是一群線框構成。*

：*突說誰話？ 驚慌樣 ）*

*俄羅斯娃娃？！)*

：*喔喔！懂了。*

*原來是 NPC 自動對話：）*

可以從提供範例更深入了解其運作原理，以下為一段測試碼：
```
<p>
    Good design will be better.
    <span class='a_font'>Ba</span>
    <span class='b_font'>Ba</span>
    <span class='c_font'>Ba</span>
    We get to make a consequence.
    // 三組 span 導入不同字體，line-height 預設高度也有所不同。
</p>
```

當一個 `<p>` 元素在瀏覽器上呈現時，文本高度由多行內文組成。每一行都包含由一個或多個行內元素 (HTML 標籤或匿名行內元素)，稱為線框。
而線框高度是基於其子元素的最高點到其子元素的最低點決定當行內容的高度。因此，瀏覽器渲染每個行內元素時，線框總是足以包含其所有子元素（預設情況下）。

![line-boxes](http://iamvdo.me/content/01-blog/30-css-avance-metriques-des-fontes-line-height-et-vertical-align/line-boxes.png)

（註 圖片來源：https://iamvdo.me/en/blog/css-font-metrics-line-height-and-vertical-align）

- 產生三行線框 (白色實線框範圍)。
- 第一行和最後一行虛線框都為匿名行內元素 (文本內容)。
- 第二行分別包含前後兩個匿名行內元素，以及中間 3 組實線框 `<span>` 行內標籤。

第二行導入三種不同字型，相較之下明顯線框最後高度由 class `c_font` 預設 line-height 決定。

>線框創建中的難點在於我們無法真正可視，更無法用 CSS 控制它。
>即使透過樣式屬性 ::first-line，也並沒有給我們任何視覺線索，證明線框的高度。

**NPC [行內熊]**：

*當理解行內元素的運行機制後，試著從 HTML 隸屬 inline 元素範圍，重新思考檢視問題：*

- 預設下 inline 元素是否可以設定寬度與高度？ 為何？
- 文本位於基礎框盒模型 (box model) 內容區域？ 可透過 CSS 樣式屬性重新改變預設值？

**To Be Continued ...**

[ 追加經驗值 ]：參考來源 [iamvdo](https://iamvdo.me/en/blog/css-font-metrics-line-height-and-vertical-align) 
