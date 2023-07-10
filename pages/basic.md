# コードの基本形

<div class="center">

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
  // ここにコードを書いていく
}
```

<div v-click id="sec-1">
<div id="red-box"></div>

← 必ず必要な「おまじない」

</div>


<div v-click id="sec-2">
<div id="blue-box"></div>

←&nbsp;

<div align="left">
main 関数、本質

この中身が実行される
</div>

</div>

</div>

<style>

.slidev-code code {
  font-size: 24px  !important;
}

pre[class*='language-'] {
  width: 800px;
}

#sec-1 {
  display: flex;
  align-items: center;

  position: absolute;
  top: 170px;
  left: 100px;
}

#red-box {
  width: 375px;
  height: 80px;
  background-color: rgba(255, 0, 0, 0.25);
  border: 2px solid red;

  margin-right: 20px;
}

#sec-2 {
  display: flex;
  align-items: center;

  position: absolute;
  top: 280px;
  left: 100px;
}

#blue-box {
  width: 375px;
  height: 110px;
  background-color: rgba(0, 0, 255, 0.25);
  border: 2px solid blue;

  margin-right: 20px;
}

</style>

---

# 出力

<center>

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    cout << "Hello,World!" << endl;
}
```

<div v-click id="sec-1">

<div id="blue-box"></div>

← 本質

</div>

</center>

<style>

.slidev-code code {
  font-size: 24px  !important;
}

pre[class*='language-'] {
  width: 900px;
}

#sec-1 {
  display: flex;
  align-items: center;

  position: absolute;
  top: 270px;
  left: 70px;
}

#blue-box {
  width: 520px;
  height: 110px;
  background-color: transparent;
  border: 2px solid blue;

  margin-right: 20px;
}

</style>

---

# 出力

<center>

```cpp
int main() {
    cout << "Hello,World!" << endl;
}
```

</center>

<v-click>

- `Hello,World!` という文字列を出力するプログラム
  - 文字列: 文字の列
    - C++ では、`""` で囲むことで文字列を表す
  - 出力: 画面に表示する、みたいなイメージ
    - プログラムが、結果として外部へ出す情報

</v-click>

<style>

.slidev-code code {
  font-size: 24px  !important;
}

pre[class*='language-'] {
  width: 900px;
  margin-bottom: 40px;
}

</style>

---

# 出力

<center>

```cpp
int main() {
    cout << "Hello,World!" << endl;
}
```

</center>

<div v-click>

<div id="cout-emp"></div>

- `cout`: 標準出力

</div>

<div v-click>

<div id="left-emp-0" class="left-emp"></div>
<div id="left-emp-1" class="left-emp"></div>

- `<<`: 矢印みたいなもん
  - `cout` にいろんなものをぶちこむ、というイメージ

</div>

<div v-click>

<div id="endl-emp"></div>

- `endl`: 改行

</div>

<div v-click>

<div id="semicolon-emp"></div>

- `;`: 文の区切り　詳しくは後述する

</div>

<style>

.slidev-code code {
  font-size: 24px  !important;
}

pre[class*='language-'] {
  width: 900px;
  margin-bottom: 20px;
}

#cout-emp {
  display: flex;
  align-items: center;

  position: absolute;
  top: 200px;
  left: 130px;

  width: 66px;
  height: 30px;
  background-color: transparent;
  border: 2px solid red;

  margin-right: 20px;
}

.left-emp {
  display: flex;
  align-items: center;

  position: absolute;

  width: 35px;
  height: 30px;
  background-color: transparent;
  border: 2px solid blue;

  margin-right: 20px;
}

#left-emp-0 {
  top: 200px;
  left: 203px;
}

#left-emp-1 {
  top: 200px;
  left: 462px;
}

#endl-emp {
  display: flex;
  align-items: center;

  position: absolute;
  top: 200px;
  left: 503px;

  width: 64px;
  height: 30px;
  background-color: transparent;
  border: 2px solid green;

  margin-right: 20px;
}

#semicolon-emp {
  display: flex;
  align-items: center;

  position: absolute;
  top: 200px;
  left: 568px;

  width: 10px;
  height: 30px;
  background-color: transparent;
  border: 2px solid black;

  margin-right: 20px;
}

</style>

---
# これ消すとなんかクリック回数多くなっちゃう slidevのバグ？
clicks: 3
---

# 出力

<center>

```cpp
int main() {
    cout << "Hello,World!" << endl;
}
```

</center>

<div id="cout-box">
<h3><span class="title">cout</span></h3>
<div class="inner">

<div v-click="1">
Hello,World!
</div>

<div v-click="2">
<br>
</div>

</div>
</div>

<div v-click-hide="2"><div class="box" id="box-0" v-click="1"></div></div>
<div v-click-hide="3"><div class="box" id="box-1" v-click="2"></div></div>

<style>

.slidev-code code {
  font-size: 24px  !important;
}

pre[class*='language-'] {
  width: 900px;
  margin-bottom: 40px;
}

#cout-box {
  min-height: calc(2.5em + 4px);

  border: 2px solid #0094D6;
  position: relative;
}
#cout-box h3{
  text-align: left;
  position: absolute;
  right: 0;
  left: 20px;
  top: -0.8em;
}
#cout-box .title{
  padding: 0.5em;
  background: #FFF;
  color: #0094D6;
}
#cout-box .inner{
  padding: 0.5em;
}

.slidev-vclick-hidden {
    block-size: 0;
}

.box {
  display: flex;
  align-items: center;

  position: absolute;

  height: 30px;
  border: 2px solid red;
}

#box-0 {
  top: 200px;
  left: 202px;

  width: 250px;
}

#box-1 {
  top: 200px;
  left: 460px;

  width: 108px;
}

</style>

---
clicks: 7
---

# 出力

<center>

```cpp
int main() {
  cout << "こんにちは。";
  cout << "Hello," << "World!" << endl;
  cout << 1234 << endl;
}
```

</center>

<div id="cout-box">
<h3><span class="title">cout</span></h3>
<div class="inner">

<div v-click="1">
<span v-click="1">
こんにちは。
</span>

<span v-click="2">
Hello,
</span>

<span v-click="3">
World!
</span>

</div>

<div v-click-hide="5">
<div v-click="4" class="br-div">
&nbsp;
</div>
</div>

<div v-click="5">
1234
</div>

<div v-click="6">
&nbsp;
</div>

</div>
</div>

<div v-click-hide="2"><div class="box" id="box-0" v-click="1"></div></div>
<div v-click-hide="3"><div class="box" id="box-1" v-click="2"></div></div>
<div v-click-hide="4"><div class="box" id="box-2" v-click="3"></div></div>
<div v-click-hide="5"><div class="box" id="box-3" v-click="4"></div></div>
<div v-click-hide="6"><div class="box" id="box-4" v-click="5"></div></div>
<div v-click-hide="7"><div class="box" id="box-5" v-click="6"></div></div>

<style>

.slidev-code code {
  font-size: 20px  !important;
}

pre[class*='language-'] {
  width: 900px;
  margin-bottom: 40px;
}

#cout-box {
  min-height: calc(2em + 4px);

  border: 2px solid #0094D6;
  position: relative;
  z-index: 10;
}
#cout-box h3{
  text-align: left;
  position: absolute;
  right: 0;
  left: 20px;
  top: -0.8em;
}
#cout-box .title{
  padding: 0.5em;
  background: #FFF;
  color: #0094D6;
}
#cout-box .inner{
  position: relative;
  z-index: 20;
  font-size: 0.8em;

  padding: 0.5em;
}

.slidev-vclick-hidden {
  block-size: 0;
}

.box {
  height: 30px;
  border-color: red;
}

#box-0 {
  top: 192px;
  left: 158px;

  width: 185px;
}

#box-1 {
  top: 222px;
  left: 158px;

  width: 140px;
}

#box-2 {
  top: 222px;
  left: 300px;

  width: 140px;
}

#box-3 {
  top: 222px;
  left: 445px;

  width: 90px;
}

#box-4 {
  top: 250px;
  left: 158px;

  width: 90px;
}

#box-5 {
  top: 250px;
  left: 252px;

  width: 90px;
}

</style>

---

# 出力

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_cv

---

# コードの構造

- C++ のコードは、**文**を並べて記述する
  - 文: コンピュータに対する1つの命令
- コンピュータは並べられた文を順に実行していく

+ 文の区切りとして、全ての文の末尾に `;` をつける
+ これを忘れるとエラーになるので気をつけよう

---

# コードの構造

<center>

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
  cout << "こんにちは。";
  cout << "Hello," << "World!" << endl;
  cout << 1234 << endl;
}
```

</center>

<div v-click class="box" id="box-0"></div>
<div v-after class="sep box" id="sep-0"></div>

<div v-click class="box" id="box-1"></div>
<div v-after class="sep box" id="sep-1"></div>

<div v-click class="box" id="box-2"></div>
<div v-after class="sep box" id="sep-2"></div>

<style>

.slidev-code code {
  font-size: 24px  !important;
}

pre[class*='language-'] {
  width: 800px;
  margin-bottom: 40px;
}

.box {
  height: 32px;
  border-color: red;
}

.sep {
  height: 32px;
  border-color: black;
  background-color: rgba(0, 0, 0, 0.25);

  width: 8px;
}

#box-0 {
  top: 307px;
  left: 132px;

  width: 298px;
}

#sep-0 {
  top: 307px;
  left: 431px;
}

#box-1 {
  top: 342px;
  left: 132px;

  width: 528px;
}

#sep-1 {
  top: 342px;
  left: 661px;
}

#box-2 {
  top: 379px;
  left: 132px;

  width: 298px;
}

#sep-2 {
  top: 379px;
  left: 431px;
}

</style>

---

# コードの構造

+ 文の命令内容は例えば…
  <ul>
    <li v-click>「これを出力して」</li>
    <li v-click>「この式を計算して」</li>
    <li v-click>「もしも〜ならこの文を実行して」</li>
    <li v-after>とか</li>
  </ul>

---

# コメント

- コードの中には、**コメント**(注釈)を書くことができる
  - コードの動作には一切影響しない
- コードに関する情報や意図などをコードの読み手に伝える

<v-click>

+ `// コメント`: 単一行コメント
  - `//`からその行が終わるまでがコメントになる
+ `/* コメント */`: 複数行コメント
  - `/*`から`*/`がまるごとコメントになる　複数行も可

</v-click>

---

# コメント

<div class="flex-box">

<div class="code-sec">

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
  int x = 0;  // コメントだよ
  
  // これもコメント
  x = 4;
  
  /* ここらへんは
  まるごと
  コメント */
  
  cout << x << endl;  // おわり
}
```

</div>

- `// コメント`: 単一行コメント
  - `//`からその行が終わるまでがコメントになる
- `/* コメント */`: 複数行コメント
  - `/*`から`*/`がまるごとコメントになる　複数行も可

</div>

<style>

.slidev-code code {
  font-size: 16px  !important;
}

pre[class*='language-'] {
  width: 420px;
}

.code-sec {
  margin-right: 40px;
}

.flex-box {
  display: flex;
}

</style>
