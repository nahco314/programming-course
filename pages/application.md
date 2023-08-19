# 範囲 for 文

- 配列の全ての要素について処理したい、というのは頻出

+ 配列の要素の総和を求めたい、みたいなときとか

---

# 範囲 for 文

- 配列 a の要素の総和を求めたい

+ 普通に書くとこんな感じ

<center>

```cpp
int res = 0;
for (int i = 0; i < a.size(); i++) {
    res += a[i];
}
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 40px;
}

.slidev-code code {
  font-size: 24px  !important;
}

</style>

---

# 範囲 for 文

- 配列 a の要素の総和を求めたい

+ 範囲 for 文という構文を使い、こう書くことができる

<center>

```cpp
int res = 0;
for (int e : a) {
    res += e;
}
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 40px;
}

.slidev-code code {
  font-size: 24px  !important;
}

</style>

---

# 範囲 for 文

- `for (要素の型 変数名 : 配列) { 中身 }` で変数に配列の要素を順に入れてループをできる

+ 使い分けとしては、「 i 番目」という情報がいらなくて、要素の中身だけが重要なときに使える

---

# 範囲 for 文

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_cg

---

# 多次元配列

- 配列は「複数の値をまとめるもの」

+ 配列自体も 1 つの値なので、「配列の配列」を扱うこともできる

---

# 多次元配列

- int の配列の配列を扱ってみる

<center>

```cpp
vector<vector<int>> a = {
  {1, 2, 3},
  {4, 6, 8},
}
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 40px;
}

.slidev-code code {
  font-size: 24px  !important;
}

</style>

---

# 多次元配列

<center>

```cpp
vector<vector<int>> a = {
  {1, 2, 3},
  {4, 6, 8},
}
```

</center>

<v-clicks>

- `int` が int
- `vector<int>` が int の配列
- `vector<vector<int>>` が int の配列の配列

</v-clicks>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-bottom: 40px;
}

.slidev-code code {
  font-size: 24px  !important;
}

</style>

---

# 多次元配列

<center>

```cpp
vector<vector<int>> a = {
  {1, 2, 3},
  {4, 6, 8},
}
```

</center>

<v-clicks>

- `{1, 2, 3}` と `{4, 6, 8}` という 2 つの要素を持つ配列

+ `a[1][2]` は `8` になる

</v-clicks>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-bottom: 40px;
}

.slidev-code code {
  font-size: 24px  !important;
}

</style>

---

# 多次元配列

<center>

```cpp
vector<vector<int>> b = {
  {1},
  {2, 3},
  {4, 5, 6},
}
```

</center>

- 各配列の長さが同じである必要はない

<style>

pre[class*='language-'] {
  width: 800px;
  margin-bottom: 40px;
}

.slidev-code code {
  font-size: 24px  !important;
}

</style>

---

# 多次元配列

- 「配列の配列」は配列が 2 つネストしているので、二次元配列と呼ぶ
- 「配列の配列の配列」なら三次元配列、普通の配列なら一次元配列

+ 二次元配列以上のネストの配列を多次元配列とか呼ぶ

---

# 多次元配列

- 多次元配列や多重ループといった、再帰的な構造というのはプログラミング初学者にとっては難しい

+ しかし、実際は単純で、正しい理解が染み付けば簡単
+ たくさんコードを書いているうちに慣れていくと想うので頑張ろう

---

# 多次元配列

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_ce

---

# 再帰関数

- 当然、関数の中で関数を呼ぶことができる

+ ある関数の中で、その関数自身を呼ぶこともできる
+ こういった呼び出しを**再帰的**な呼び出しと呼ぶ

- 再帰呼び出しを含む関数を再帰関数と呼ぶ

---

# 再帰関数

- 例を見てみよう

<v-clicks>

+ n の階乗 n! = 1 * 2 * 3 * ... * (n - 1) * n
+ 入れ替えると: n! = n * (n - 1) * ... * 3 * 2 * 1
+ こう見れる: n! = n * (n - 1)!

</v-clicks>

---

# 再帰関数

- 例を見てみよう
- n の階乗を計算する関数を普通に実装すると...

<center>

```cpp
int factorial(int n) {
  int res = 1;
  for (int i = 1; i <= n; i++) {
    res *= i;
  }
  return res;
}
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 25px;
}

.slidev-code code {
  font-size: 20px  !important;
}

</style>

---

# 再帰関数

- 例を見てみよう
- 再帰で実装すると...

<center>

```cpp
int factorial(int n) {
  if (n == 1) {
    return 1;
  }
  return n * factorial(n - 1);
}
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 25px;
}

.slidev-code code {
  font-size: 20px  !important;
}

</style>

---
clicks: 19
---

# 再帰関数

- `factorial(4)` を計算することを考える

<div id="main">

<div id="code-sec">

```cpp
int factorial(int n) {
  if (n == 1) {
    return 1;
  }
  return n * factorial(n - 1);
}
```

</div>

<div id="stack-box">
<div class="inner">

<div v-click-hide="19">
<div v-click="1">

`factorial(4)`

</div>
</div>

<div v-click-hide="17">
<div v-click="4">

`factorial(3)`

</div>
</div>

<div v-click-hide="15">
<div v-click="7">

`factorial(2)`

</div>
</div>

<div v-click-hide="13">
<div v-click="10">

`factorial(1)`

</div>
</div>

</div>
</div>

</div>

<div v-click-hide="2"><div class="box func-box" v-click="1"></div></div>
<div v-click-hide="3"><div class="box return-box" v-click="2"></div></div>
<div v-click-hide="4"><div class="box call-box" v-click="3"></div></div>

<div v-click-hide="5"><div class="box func-box" v-click="4"></div></div>
<div v-click-hide="6"><div class="box return-box" v-click="5"></div></div>
<div v-click-hide="7"><div class="box call-box" v-click="6"></div></div>

<div v-click-hide="8"><div class="box func-box" v-click="7"></div></div>
<div v-click-hide="9"><div class="box return-box" v-click="8"></div></div>
<div v-click-hide="10"><div class="box call-box" v-click="9"></div></div>

<div v-click-hide="11"><div class="box func-box" v-click="10"></div></div>
<div v-click-hide="12"><div class="box" id="box-0" v-click="11"></div></div>
<div v-click-hide="13"><div class="box" id="box-1" v-click="12"></div></div>

<div v-click-hide="14"><div class="box call-box" v-click="13"></div></div>
<div v-click-hide="15"><div class="box return-box" v-click="14"></div></div>

<div v-click-hide="16"><div class="box call-box" v-click="15"></div></div>
<div v-click-hide="17"><div class="box return-box" v-click="16"></div></div>

<div v-click-hide="18"><div class="box call-box" v-click="17"></div></div>
<div v-click-hide="19"><div class="box return-box" v-click="18"></div></div>

<style>

pre[class*='language-'] {
  width: 450px;
  margin-top: 40px;
}

.slidev-code code {
  font-size: 20px  !important;
}

.box {
  border-color: orange;
}

.func-box {
  top: 238px;
  left: 70px;

  width: 375px;
  height: 192px;
}

.return-box {
  top: 365px;
  left: 95px;

  width: 345px;
  height: 30px;
}

.call-box {
  top: 365px;
  left: 228px;

  width: 210px;
  height: 30px;
}

#box-0 {
  top: 272px;
  left: 95px;

  width: 170px;
  height: 95px;
}

#box-1 {
  top: 272px;
  left: 95px;

  width: 170px;
  height: 95px;
}

#box-1 {
  top: 305px;
  left: 120px;

  width: 112px;
  height: 30px;
}

#main {
  display: flex;
}

#code-sec, #stack-box {
  flex: 1;
}

#stack-box {
  min-height: calc(2.5em + 4px);

  margin: 40px;

  border: 2px solid #0094D6;
  position: relative;
}

#stack-box h3{
  text-align: left;
  position: absolute;
  right: 0;
  left: 20px;
  top: -0.8em;
}
#stack-box .title{
  padding: 0.5em;
  background: #FFF;
  color: #0094D6;
}
#stack-box .inner{
  padding: 0.5em;
}

</style>

---

# 再帰関数

- 演習問題
  - むずめかも
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_cc
