# 型

- C++ において、全ての値には**型**がある
- 型: 「値の種類」

+ 今までに扱ったことのある型

<center>

| 型名       | 内容  | 例                |
|----------|-----|------------------|
| `int`    | 整数  | `42`             |
| `float`  | 小数  | `0.25`           |
| `string` | 文字列 | `"Hello,World!"` |

</center>

<style>

.slidev-layout table {
  width: 700px;
  margin-top: 12px;
}

</style>

<!--
型という新概念を丁寧に説明する

いままでに整数と小数と文字列を使ったことがあるので、それを例に値に種類があるという概念を説明
-->

---

# 型

- 全ての値には型があるので、当然全ての式に型がある

<center>

| 式             | 型       |
|---------------|---------|
| `1 + 2`       | `int`   |
| `7 / 3`       | `int`   |
| `7.0 / 3`     | `float` |
| `(2 + 3) * 4` | `int`   |

</center>

<style>

.slidev-layout table {
  width: 700px;
  margin-top: 30px;
}

</style>

<!--
厳密に言うと、例えば整数や文字列のリテラルも式で、四則演算などと同じようにそれぞれの値に評価されるのであって、「リテラル(値)が型を持つ」と「全ての式が型を持つ」はそこまで違うことを言っていない

が、そういう理解は難しいので、あえて「リテラル」と「値」の概念を少し混同したまま説明をしていく
-->

---

# 型

- 型は、その値がどのように振る舞うか(扱われるか)を定義する
  - というと難しそうだが、要するに「型によって扱いが変わる」

+ 例えば、型は割り算の挙動を定義する
  - `int / int` → `int`
  - `int / float` → `float`
  - `float / int` → `float`
  - `float / float` → `float`

<!--
ここは説明が難しいが、型(=値の種類)が(どういう値なのかを判別するために)必要であるというのは直感的に明らかなのを、形式的な言葉使いで再定義してやる、という感じかな

整数/小数による割り算や挙動の違いは四則演算のところで既に説明済みなので、それを用いて型による扱いの違いを例示する

ちなみに、型が値の振る舞いを定義するものであるという理解は、たしか型理論的には正しいものではないが、C++を学ぶ上では十分だろう
-->

---

# 変数

- 値を読み書きする*記憶域*
  - 「値を格納できる箱」というイメージ

<v-click>

+ 例を見てみよう

</v-click>

<!--
「変数というのは値を読み書きできる記憶域です。といっても、記憶域って何かわかんないですよね。プログラミング初心者に向けた説明だと、変数はよく「箱」に例えられます。変数という箱の中に値を入れたり、取り出したりできるイメージです」みたいな

C++における変数はあくまでもメモリ上の領域であるから、単に箱と言ってしまうより、少し難しいものという前提を置いた上で箱という例を出したい
-->

---
clicks: 6
---

# 変数

<div id="main">

```cpp
int main() {
  int num;

  num = 10;

  cout << num << endl;  // 10
  
  num = 4;
  
  cout << num * 2 << endl;  // 8
}
```

<div v-click="1">

<div id="num-box">
<h3><span class="title">num</span></h3>
<div class="inner">

<div v-click-hide="4">
<div v-click="2">
10
</div>
</div>

<div v-click="4">
4
</div>

</div>
</div>

</div>

</div>

<div v-click-hide="2">
<div v-click="1">

<div class="box" id="box-0"></div>

- `int num;`
  - 変数の**宣言**
  - `int` 型の値を扱う、`num` という名前の変数

</div>
</div>

<div v-click-hide="3">
<div v-click="2">

<div class="box" id="box-1"></div>

- `num = 10;`
  - `num` に `10` を**代入**する
  - 代入: 変数に値を入れる

</div>
</div>

<div v-click-hide="4">
<div v-click="3">

<div class="box" id="box-2"></div>

- `cout << num << endl;`
  - `num` の中身を出力
  - 変数の中身を取り出すことを、**参照**するという

</div>
</div>

<div v-click-hide="5">
<div v-click="4">

<div class="box" id="box-3"></div>

- `num = 4;`
  - `num` に `4` を代入する

</div>
</div>

<div v-click-hide="6">
<div v-click="5">

<div class="box" id="box-4"></div>

- `cout << num * 2 << endl;`
  - `num` の中身を2倍して出力する

</div>
</div>

<style>

pre[class*='language-'] {
  width: 550px;
}

.slidev-code code {
  font-size: 12px;
  height: 600px  !important;
}

#main {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

#num-box {
  height: 150px;
  width: 150px;

  border: 2px solid #0094D6;
  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;

  margin-left: 120px;
}
#num-box h3{
  text-align: center;
  position: absolute;
  right: 0;
  left: 0;
  top: -1em;
}
#num-box .title{
  font-size: 30px;

  padding: 0.5em;
  background: #FFF;
  color: #0094D6;
}
#num-box .inner{
  font-size: 64px;

  margin-top: -16px;
}

.box {
  height: 24px;
  border-color: orange;
}

#box-0 {
  top: 188px;
  left: 108px;

  width: 70px;
}

#box-1 {
  top: 224px;
  left: 108px;

  width: 74px;
}

#box-2 {
  top: 260px;
  left: 108px;

  width: 155px;
}

#box-3 {
  top: 296px;
  left: 108px;

  width: 70px;
}

#box-4 {
  top: 332px;
  left: 108px;

  width: 184px;
}

.slidev-vclick-hidden {
    block-size: 0;
}

</style>

<!--
変数の基本的な使い方を説明する

宣言は「型名」と「変数名」という構成をしっかり説明する

代入は、数学における=と意味合いが違うことを説明する

参照は、出力や四則演算の例を使いながら、「整数リテラルのなどと同じように、変数名を書けば参照して値として使える」ということを理解させていく
-->

---

# 変数 - 余談

- 変数の宣言と最初の代入(初期化とも呼ぶ)は同時にできる
- int 型に限らず、様々な型の変数を使うことができる

<center>

```cpp
int main() {
  int num = 10;
  float per = 0.25;

  cout << num * per << endl;  // 2.5
  
  string greeting = "Hello!";
  
  cout << greeting << endl;  // Hello!
}
```

</center>

<style>

pre[class*='language-'] {
  margin-top: 20px;
  width: 760px;
}

</style>

---

# 変数

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_cs

---

# 入力

- プログラムは `cout` で外部に出力を行うが、逆に外部からの**入力**を受け取ることもできる

<center>

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
  int num;
  
  cin >> num;
  
  cout << num * 10 << endl;
}
```

</center>

<style>

pre[class*='language-'] {
  margin-top: 20px;
  width: 760px;
}

.slidev-code code {
  font-size: 16px;
}

</style>

<!--
コンソールとか標準入力とか、初心者はわからないので、「プログラムが外部と情報をやり取りするための手段」というのを丁寧に導入する
-->

---

# 入力

<center>

```cpp
int main() {
  int num;
  
  cin >> num;
  
  cout << num * 10 << endl;
}
```

</center>

- `cin >> 変数;` で変数に入力を受け取る
  - `cout` は out なので出力、`cin` は in なので入力

<style>

pre[class*='language-'] {
  margin-bottom: 30px;
  width: 760px;
}

.slidev-code code {
  font-size: 20px;
}

</style>

---

# 入力

<center>

```cpp
int main() {
  int num;
  
  cin >> num;
  
  cout << num * 10 << endl;
}
```

</center>

- `cout` は「標準出力」へ出力を行う
- `cin` は「標準入力」から入力を受け取る

<style>

pre[class*='language-'] {
  margin-bottom: 30px;
  width: 760px;
}

.slidev-code code {
  font-size: 20px;
}

</style>

<!--
標準入出力という用語の定義
-->

---
clicks: 4
---

# 入力

<div id="main">

<div id="code-sec">

```cpp
int main() {
  int num;
  
  cin >> num;
  
  cout << num * 10 << endl;
}
```

</div>

<div id="var-sec">

<div v-click="1">

<div class="var-box">
<h3><span class="title">num</span></h3>
<div class="inner">

<div v-click="2">
42
</div>

</div>
</div>

</div>

</div>

</div>

<div id="cin-box">
<h3><span class="title">cin</span></h3>
<div class="inner">

42

</div>
</div>

<div id="cin-cover">

<div v-click="2" class="box cin-cover-box" id="cover-0"></div>

</div>

<div v-click-hide="2"><div v-click="1" class="box code-box" id="box-0"></div></div>
<div v-click-hide="3"><div v-click="2" class="box code-box" id="box-1"></div></div>
<div v-click-hide="4"><div v-click="3" class="box code-box" id="box-2"></div></div>

<style>

#main {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.slidev-code code {
  font-size: 20px  !important;
}

pre[class*='language-'] {
  width: 550px;
  margin-bottom: 40px;
}

#cin-box {
  min-height: calc(2.5em + 4px);

  border: 2px solid forestgreen;
  position: relative;
}
#cin-box h3{
  text-align: left;
  position: absolute;
  right: 0;
  left: 20px;
  top: -0.8em;
}
#cin-box .title{
  padding: 0.5em;
  background: #FFF;
  color: forestgreen;
}
#cin-box .inner{
  padding: 0.5em;
}

.var-box {
  height: 150px;
  width: 150px;

  border: 2px solid #0094D6;
  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;

  margin-left: 120px;
}
.var-box h3{
  text-align: center;
  position: absolute;
  right: 0;
  left: 0;
  top: -1em;
}
.var-box .title{
  font-size: 30px;

  padding: 0.5em;
  background: #FFF;
  color: #0094D6;
}
.var-box .inner{
  font-size: 64px;

  margin-top: -16px;
}

#cin-cover {
}

.cin-cover-box {
  border: none;
  background-color: #1b1b1b;
}

#cover-0 {
  top: 460px;
  left: 72px;

  height: 45px;
  width: 32px;
}

.code-box {
  height: 30px;
  border-color: orange;
}

#box-0 {
  top: 198px;
  left: 120px;


  width: 100px;
}

#box-1 {
  top: 259px;
  left: 120px;


  width: 136px;
}

#box-2 {
  top: 319px;
  left: 120px;


  width: 306px;
}

</style>

<!--
cinによって標準出力上の文字列が消費されていくという感じを表現したい
-->

---
clicks: 7
---

# 入力

<div id="main">

<div id="code-sec">

```cpp
int main() {
  int a, b;
  
  string c, s;
  
  cin >> a >> b >> c;
  
  cin >> s;
}
```

</div>

<div id="var-sec-outer">

<div id="var-sec-0">

<div v-click="1" class="var-box">
<h3><span class="title">a</span></h3>
<div class="inner">

<div v-click="3">
5
</div>

</div>
</div>

<div v-click="1" class="var-box">
<h3><span class="title">b</span></h3>
<div class="inner">

<div v-click="4">
12
</div>

</div>
</div>

</div>

<div id="var-sec-0">

<div v-click="2" class="var-box">
<h3><span class="title">c</span></h3>
<div class="inner">

<div v-click="5">
"24"
</div>

</div>
</div>

<div v-click="2" class="var-box">
<h3><span class="title">s</span></h3>
<div class="inner">

<div v-click="6">
"abc"
</div>

</div>
</div>

</div>

</div>

</div>

<div id="cin-box">
<h3><span class="title">cin</span></h3>
<div class="inner">

5 12

24

abc

</div>
</div>

<div id="cin-cover">

<div v-click="3" class="box cin-cover-box" id="cover-0"></div>
<div v-click="4" class="box cin-cover-box" id="cover-1"></div>
<div v-click="5" class="box cin-cover-box" id="cover-2"></div>
<div v-click="6" class="box cin-cover-box" id="cover-3"></div>

</div>

<div v-click-hide="2"><div v-click="1" class="box code-box" id="box-0"></div></div>
<div v-click-hide="3"><div v-click="2" class="box code-box" id="box-1"></div></div>
<div v-click-hide="6"><div v-click="3" class="box code-box" id="box-2"></div></div>
<div v-click-hide="7"><div v-click="6" class="box code-box" id="box-3"></div></div>

<style>

#main {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.slidev-code code {
  font-size: 16px  !important;
}

pre[class*='language-'] {
  width: 550px;
  margin-bottom: 20px;
}

#cin-box {
  border: 2px solid forestgreen;
  position: relative;
}
#cin-box h3{
  text-align: left;
  position: absolute;
  right: 0;
  left: 20px;
  top: -0.8em;
}
#cin-box .title{
  padding: 0 0.5em;
  background: #FFF;
  color: forestgreen;
}
#cin-box .inner{
  font-size: 20px;
  padding: 0.8em;
}
#cin-box p {
  margin: 0;
}

#var-sec-0, #var-sec-1 {
  margin-left: 30px;
  margin-bottom: 30px;

  display: flex;
}

.var-box {
  height: 75px;
  width: 75px;

  border: 2px solid #0094D6;
  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;

  margin-left: 20px;
}
.var-box h3{
  text-align: center;
  position: absolute;
  right: 0;
  left: 0;
  top: -1em;
}
.var-box .title{
  font-size: 30px;

  padding: 0 0.5em;
  background: #FFF;
  color: #0094D6;
}
.var-box .inner{
  font-size: 28px;

  margin-top: -8px;
}

#cin-cover {
}

.cin-cover-box {
  border: none;
  background-color: #1b1b1b;
}

#cover-0 {
  top: 445px;
  left: 72px;

  height: 24px;
  width: 15px;
}

#cover-1 {
  top: 445px;
  left: 72px;

  height: 24px;
  width: 50px;
}

#cover-2 {
  top: 468px;
  left: 72px;

  height: 24px;
  width: 50px;
}

#cover-3 {
  top: 490px;
  left: 72px;

  height: 24px;
  width: 50px;
}

.code-box {
  height: 24px;
  border-color: orange;
}

#box-0 {
  top: 192px;
  left: 140px;

  width: 92px;
}

#box-1 {
  top: 240px;
  left: 140px;

  width: 120px;
}

#box-2 {
  top: 288px;
  left: 140px;

  width: 188px;
}

#box-3 {
  top: 337px;
  left: 140px;

  width: 92px;
}

</style>

<!--
複数回の入力を行うと標準入力の文字列が消費されていく、ということをしっかり説明する

あと入力のひと区切りが空白や改行になることも説明

標準入力から読み取られた文字列がどのように解釈されるかは入力先の型に依存することも理解させる
-->

---

# 入力

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_cr
