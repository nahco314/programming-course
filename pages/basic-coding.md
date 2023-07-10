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

<style>

.slidev-code code {
  font-size: 24px  !important;
}

pre[class*='language-'] {
  width: 900px;
  margin-bottom: 40px;
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

  width: 66px;
  height: 30px;
  background-color: transparent;
  border: 2px solid green;

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

# セミコロン

- 前述したが、C++ では文の区切りとして、全ての文の末尾に `;` をつける

```cpp
#include <bits/stdc++.h>
using namespace std;
 
int main() {
  cout << "こんにちは。";
  cout << "Hello," << "World!" << endl;
  cout << 1234 << endl;
}
```

<style>

pre[class*='language-'] {
  margin-top: 40px;
}

</style>

---

# 四則演算

- C++では整数を扱うことができる

```cpp
#include <bits/stdc++.h>
using namespace std;
 
int main() {
  cout << "こんにちは。";
  cout << "Hello," << "World!" << endl;
  cout << 1234 << endl;
}
```

<div id="int-emp-sec">
<div id="int-emp-box"></div>
↑これ
</div>

<style>

pre[class*='language-'] {
  margin-top: 20px;
}

#int-emp-sec {
  position: absolute;

  text-align: center;
  font-size: 16px;

  top: 367px;
  left: 169px;
}

#int-emp-box {
  height: 25px;
  width: 45px;

  border: 2px solid red;
}

</style>

---

# 四則演算

- 整数を扱う簡単な計算もできる

<center>

```cpp
int main() {
  cout << 1 + 1 << endl;  // 2  足し算
  cout << 3 - 4 << endl;  // -1 引き算
  cout << 2 * 3 << endl;  // 6  掛け算
  cout << 7 / 3 << endl;  // 2  割り算
  cout << 7 % 3 << endl;  // 1  割り算の"あまり"

  cout << +4 << endl;  // 4  プラス記号
  cout << -3 << endl;  // -3 マイナス記号

  cout << 2 + 3 * 4 << endl;    // 14
  cout << (2 + 3) * 4 << endl;  // 30
}
```

</center>

<style>

pre[class*='language-'] {
  width: 650px;
  margin-top: 20px;
}

</style>

---

# 四則演算

<center>

```cpp
cout << 1 + 1 << endl;  // 2  足し算
```

</center>

- 普通に足し算

<style>

.slidev-code code {
  font-size: 30px  !important;
}

pre[class*='language-'] {
  width: 840px;
  margin-bottom: 40px;
}

</style>

---

# 四則演算

<center>

```cpp
cout << 3 - 4 << endl;  // -1 引き算
```

</center>

- 普通に引き算
- 負の整数も扱えるよ

<style>

.slidev-code code {
  font-size: 30px  !important;
}

pre[class*='language-'] {
  width: 840px;
  margin-bottom: 40px;
}

</style>

---

# 四則演算

<center>

```cpp
cout << 2 * 3 << endl;  // 6  掛け算
```

</center>

- 掛け算　記号は「×」とかじゃなくて `*` なので注意しよう
  - `*`: アスタリスク

<style>

.slidev-code code {
  font-size: 30px  !important;
}

pre[class*='language-'] {
  width: 840px;
  margin-bottom: 40px;
}

</style>

---

# 四則演算

<center>

```cpp
cout << 7 / 3 << endl;  // 2  割り算
```

</center>

- 割り算　記号は `/`
  - `/`: スラッシュ
  - / の左が分子、右が分母だと考えると、分数の表示を平たくしたみたいに見える

+ 整数同士の割り算は、答えが切り捨てで整数になる

<style>

.slidev-code code {
  font-size: 30px  !important;
}

pre[class*='language-'] {
  width: 840px;
  margin-bottom: 40px;
}

</style>

---

# 四則演算

<center>

```cpp
cout << 7 % 3 << endl;  // 1  割り算の"あまり"
```

</center>

- 割り算のあまり

+ 7÷3は2あまり1なので、`7 % 3` は `1` となる

<style>

.slidev-code code {
  font-size: 30px  !important;
}

pre[class*='language-'] {
  width: 840px;
  margin-bottom: 40px;
}

</style>

---

# 四則演算

<center>

```cpp
cout << +4 << endl;  // 4  プラス記号
cout << -3 << endl;  // -3 マイナス記号
```

</center>

- 普通にプラスとマイナス

<style>

.slidev-code code {
  font-size: 30px  !important;
}

pre[class*='language-'] {
  width: 840px;
  margin-bottom: 40px;
}

</style>

---

# 四則演算 - 優先順位

- これらの演算には優先順位がある
- 優先順位は我々が普段使っているものと同じ
  - `*/%` → `+-` の順で計算される
  
+ `()` で括ることで先に計算させることもできる

---

# 四則演算 - 優先順位

<center>

```cpp
cout << 2 + 3 * 4 << endl;    // 14
cout << (2 + 3) * 4 << endl;  // 30
```

</center>

- 掛け算が先に計算されるので、上の式は `14` になる
- `()` でくくったとこは先に計算されるので、下の式は `30` になる

<style>

.slidev-code code {
  font-size: 30px  !important;
}

pre[class*='language-'] {
  width: 840px;
  margin-bottom: 40px;
}

</style>
