
# DOM について　

2020.06.22

## 参考サイト

MDN サイト
- https://developer.mozilla.org/ja/docs/Web/API/Document_Object_Model/Introduction

---

DOMで操作するもの
- HTMLドキュメント
- XMLドキュメント

DOMの骨組み
- コンテンツ（情報、文章など）
- 構造（ツリー）

---

### DOMツリーとは、こんなもの

左はコード  
右の矢印を押してみて  
- https://www.w3schools.com/howto/tryit.asp?filename=tryhow_js_treeview

---

### document

親玉、ボス
ここから全てが始まる

---

### node (ノード)

DOMツリーの  
枝一つ一つを  
**ノード**と呼ぶ

---

### element (要素)

要素はノードと似た様なもの
今の段階では
同じ様に使うと覚える

---

### tag (タグ)

**タグ**は
<html></html>
<div></div>
<a></a>
と２つペアとなったもの
それぞれ用途が違う

---

### タグの種類を網羅してみる

HTMLクリックリファランス
- http://www.htmq.com/html/
良く使うタグを網羅
- https://weblan3.com/html/
初心者タグ２０選
- https://dhw-s.com/blog/knowledge/html-tag-20/
初心者〜中級者タグ
https://web-camp.io/magazine/archives/27519

---

### attribute (属性)

MDN サイト
https://developer.mozilla.org/ja/docs/Web/HTML/Attributes

属性は

<div id="属性1" class="属性2"></div>

のように
タグの中にいれられる
タグのようなもの

---

NodeList [MDN Link](https://developer.mozilla.org/ja/docs/Web/API/Document_Object_Model/Introduction)

> nodeList は、 document.getElementsByTagName() で返されるものなど要素の配列です。 nodeList 中の項目は、インデックスを使って以下の２つの方法で取得できます。
> list.item(1)
> list[1]
> この二つの方法は等価です。最初の方法では、 item() は nodeList オブジェクトの一つの関数です。後者の方は、一般的な配列の構文を使い、リスト中の二つ目の項目を取得しています。

---

### <良く分からない　２０２０.０６．２２>

NamedNodeMap [MDN Link](https://developer.mozilla.org/ja/docs/Web/API/Document_Object_Model/Introduction)

> namedNodeMap は配列のようですが、名前またはインデックスによって項目にアクセスきますが、後者は項目がリスト中に特定の順番で並んでいる訳ではないので、列挙するのに便利であるだけです。このために namedNodeMap には item() メソッドがあり、 namedNodeMap に項目を追加したり、削除したりすることができます。

---

### <良く分からない２　２０２０.０６．２２>

#### DOM インタフェース

何となく  
DOMのオブジェクトが  
どのオブジェクトが何処にあるのかの構造みたいなもの  
**オブジェクトのツリー構造**みたいなものが  
複雑に絡み合っている  
と覚える

---

コアインタフェース [MDN Link](https://developer.mozilla.org/ja/docs/Web/API/Document_Object_Model/Introduction)

> Document と window オブジェクトが一般的に DOM プログラミングの中で最もよく使われます。簡単に言うと、 window オブジェクトはブラウザーのようなものを表現し、 document オブジェクトは文書のルート自身です。 Element は一般的な Node インターフェイスを継承していて、あわせてこの 2 つのインターフェイスはここの要素で使われる多くの関数と属性を提供します。前節での table オブジェクトの例のように、これの要素はそれぞれが持つデータを扱うための特定のインターフェイスを持っている場合があります。

既に習ったので  
getElementBy系は排除  

代わりに下を使用
- document.querySelectorAll()
- document.querySelector()

- document.createElement(name)
- parentNode.appendChild(node)
- element.innerHTML
- element.style.left
- element.setAttribute()
- element.getAttribute()
- element.addEventListener()
- window.content
- window.onload
- console.log()
- window.scrollTo()

- <s> document.getElementById(id) </s>
- <s> document.getElementsByTagName(name) </s>
