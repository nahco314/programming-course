# 配列

- 配列: 複数の値を格納・管理する値
- 変数が「値を格納できる箱」なら、配列はそれが一列に並んでいる感じ

+ 配列に格納される値のこと**要素**という

---

# 配列

- C++ で配列を扱うには、vector という型を使う
- `vector<要素の型名>` で「ある型を要素に持つ配列型」を表す
  - `vector<要素の型名> 変数名;` で配列の変数の宣言

+ `変数名 = { 要素1, 要素2, ... };` で配列の変数に値を代入
+ `配列[i]` で i 番目の要素を参照
  - i 番目というのは、「左から i 番目」みたいな感じ
  - 一番左が 0 番目、その右が 1 番目...というふうに**0から数える**

---
clicks: 3
---

# 配列

<center>

```cpp
int main() {
  vector<int> nums;
 
  nums = { 25, 100, 64 };
 
  cout << nums[0] << endl;
}
```

</center>

<div v-click="1">

<div id="nums-box">
<h3><span class="title">nums</span></h3>
<div v-click="2" class="inner">

<div id="elt-box">
<h3><span class="title">0</span></h3>
<div class="inner">

25

</div>
</div>

<div id="elt-box">
<h3><span class="title">1</span></h3>
<div class="inner">

100

</div>
</div>

<div id="elt-box">
<h3><span class="title">2</span></h3>
<div class="inner">

64

</div>
</div>

</div>
</div>

</div>

<div v-click-hide="2">
<div v-click="1" class="box" id="box-0"></div>
</div>

<div v-click-hide="3">
<div v-click="2" class="box" id="box-1"></div>
</div>

<div v-click-hide="4">
<div v-click="3" class="box" id="box-2"></div>
</div>

<style>

pre[class*='language-'] {
  width: 750px;
}

#nums-box {
  min-height: calc(2.5em + 4px);

  border: 2px solid #0094D6;
  position: relative;

  margin-top: 20px;
}
#nums-box h3{
  text-align: center;
  position: absolute;
  right: 0;
  left: 20px;
  top: -0.8em;
}
#nums-box .title{
  padding: 0 0.5em;
  background: #FFF;
  color: #0094D6;
}
#nums-box .inner{
  display: flex;
  justify-content: center;

  padding: 35px 0 20px 0;
}

#elt-box {
  height: 100px;
  width: 100px;

  border: 2px solid #0094D6;
  position: relative;
  z-index: -20;

  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;

  margin-left: -2px;
}
#elt-box h3{
  text-align: center;
  position: absolute;
  right: 0;
  left: 0;
  top: -1em;
}
#elt-box .title{
  font-size: 30px;

  padding: 0 0.5em;
  background: #FFF;
  color: #0094D6;
}
#elt-box .inner{
  font-size: 44px;

  margin-top: -16px;
}

.box {
  height: 24px;
  border-color: orange;
}

#box-0 {
  top: 184px;
  left: 150px;

  width: 170px;
}

#box-1 {
  top: 232px;
  left: 150px;

  width: 227px;
}

#box-2 {
  top: 280px;
  left: 150px;

  width: 236px;
}

</style>

---

# 配列 - いろんな操作

<v-clicks>

- `nums[i] = 10` で nums の i 番目に 10 を代入
- `nums.size()` で nums の要素数を取得
- `vector<int> a(N);` で `vector<int>` 型の a を宣言し、**aの要素数をNとする**
  - N個の箱が予め用意される感じ(それぞれの箱は空)

</v-clicks>

---

# 配列 - 使い方の例

- 「いくつかの整数を受け取って、その総和を出力するプログラム」を書きたい

+ 最初に整数の数 N が入力され、その後に N 個の整数が入力される

---
clicks: 18
---

# 配列 - 使い方の例

<div id="main">

<div id="code-sec">

```cpp
int main() {
  int n;
  cin >> n;
  
  vector<int> a(n);
  for (int i = 0; i < n; i++) {
    cin >> a[i];
  }
  
  int sum = 0;
  for (int i = 0; i < n; i++) {
    sum += a[i];
  }
  
  cout << sum << endl;
}
```

</div>

<div id="right-sec">

標準入力

```text
5
2 4 8 10 5
```

<div v-click="1"></div>
<div v-click="2"></div>

<div v-click="3">

<div id="nums-box">
<h3><span class="title">nums</span></h3>
<div class="inner">

<div id="elt-box">
<h3><span class="title">0</span></h3>
<div v-click="5" class="inner">

2

</div>
</div>

<div id="elt-box">
<h3><span class="title">1</span></h3>
<div v-click="6" class="inner">

4

</div>
</div>

<div id="elt-box">
<h3><span class="title">2</span></h3>
<div v-click="7" class="inner">

8

</div>
</div>

<div id="elt-box">
<h3><span class="title">3</span></h3>
<div v-click="8" class="inner">

10

</div>
</div>

<div id="elt-box">
<h3><span class="title">4</span></h3>
<div v-click="9" class="inner">

5

</div>
</div>

</div>
</div>

</div>

</div>

</div>

<div id="under">

<div v-click-hide="2">
<div v-click="1">

- `int n;`

</div>
</div>

<div v-click-hide="3">
<div v-click="2">

- `cin >> n;`

</div>
</div>

<div v-click-hide="4">
<div v-click="3">

- `vector<int> a(n);`

</div>
</div>

<div v-click-hide="10">
<div v-click="5">

- `cin >> a[i];`

</div>
</div>

<div v-click-hide="11">
<div v-click="10">

- `int sum = 0;`

</div>
</div>

<div v-click-hide="17">
<div v-click="12">

- `sum += a[i];`

</div>
</div>

<div v-click-hide="18">
<div v-click="17">

- `cout << sum << endl;`

</div>
</div>

</div>

<style>

#main {
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-align: center;
}

#code-sec {
  width: 300px;
}

#right-sec {
  display: flex;
  flex-direction: column;
  align-items: center;

  width: 400px;
}

#code-sec code {
  font-size: 10px;
}

#right-sec code {
  font-size: 32px;
}

#right-sec pre[class*='language-'] {

  width: 400px;
}

#nums-box {
  min-height: calc(2.5em + 4px);

  border: 2px solid #0094D6;
  position: relative;

  width: fit-content;

  padding: 0 20px;
}
#nums-box h3{
  text-align: center;
  position: absolute;
  right: 0;
  left: 0;
  top: -0.8em;
}
#nums-box .title{
  font-size: 20px;

  padding: 0 0.5em;
  background: #FFF;
  color: #0094D6;
}
#nums-box .inner{
  display: flex;
  justify-content: center;

  padding: 24px 0 20px 0;
}

#elt-box {
  height: 50px;
  width: 50px;

  border: 2px solid #0094D6;
  position: relative;
  z-index: -20;

  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;

  margin-left: -2px;
}
#elt-box h3{
  text-align: center;
  position: absolute;
  right: 0;
  left: 0;
  top: -1em;
}
#elt-box .title{
  font-size: 20px;

  padding: 0 0.5em;
  background: #FFF;
  color: #0094D6;
}
#elt-box .inner{
  font-size: 24px;

  margin-top: -8px;
}

.box {
  height: 24px;
  border-color: orange;
}

#box-0 {
  top: 184px;
  left: 150px;

  width: 170px;
}

#box-1 {
  top: 232px;
  left: 150px;

  width: 227px;
}

#box-2 {
  top: 280px;
  left: 150px;

  width: 236px;
}

#under {
  margin-top: 10px;
}

#under code {
  font-size: 30px;
}

#under .slidev-vclick-hidden {
  block-size: 0;
}

</style>

---

# 配列

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_cj

---

# 配列 - もっといろんな操作

- `a.push_back(e);` で a の末尾に e を追加
- `a.pop_back();` で a の末尾の要素を削除
- `a.empty();` で a が空か判定

---

# 文字列は文字の列

- C++ には文字を表す、`char` という型が存在する
  - 1 文字を `''` で囲む

+ string 型は、char の列
  - `vector<char>` のようなイメージ
  - 実際には vector とは異なる実装ぽい

---

# 文字列は文字の列

- string に対して vector と似たような操作ができる

+ `s[i] = 'a';`
+ `s.size()`
+ `s.push_back('a');`
+ `s.pop_back();`

---
clicks: 6
---

# 文字列は文字の列

<center>

```cpp
int main() {
  string a = "abc";
 
  a[0] = 'd';
    
  a.push_back('x');
  a.push_back('y');
  
  a.pop_back();
  
  cout << a.size() << endl;
  cout << a << endl;
  cout << a[1] << endl;
}
```

</center>

<div id="s-display">

<div v-click-hide="2">
<div v-click="1">s: abc</div>
</div>

<div v-click-hide="3">
<div v-click="2">s: dbc</div>
</div>

<div v-click-hide="4">
<div v-click="3">s: dbcx</div>
</div>

<div v-click-hide="5">
<div v-click="4">s: dbcxy</div>
</div>

<div v-click-hide="6">
<div v-click="5">s: dbcx</div>
</div>

</div>

<div v-click-hide="2"><div v-click="1" class="box" id="box-0"></div></div>
<div v-click-hide="3"><div v-click="2" class="box" id="box-1"></div></div>
<div v-click-hide="4"><div v-click="3" class="box" id="box-2"></div></div>
<div v-click-hide="5"><div v-click="4" class="box" id="box-3"></div></div>
<div v-click-hide="6"><div v-click="5" class="box" id="box-4"></div></div>
<div v-click-hide="7"><div v-click="6" class="box" id="box-5"></div></div>

<center>

<div v-click="6" id="output-sec">

```text
4
dbcx
b
```

</div>

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-bottom: 20px;
}

.slidev-code code {
  font-size: 12px  !important;
}

#output-sec pre[class*='language-'] {
  width: 840px;
  margin-top: -10px;
}

#output-sec .slidev-code code {
  font-size: 16px  !important;
}

#s-display {
  margin-left: 45px;
  font-size: 50px;
}

#s-display code {
  font-size: 50px;
}

.box {
  height: 20px;
  border-color: orange;
}

#box-0 {
  top: 178px;
  left: 120px;

  width: 130px;
}

#box-1 {
  top: 214px;
  left: 120px;

  width: 85px;
}

#box-2 {
  top: 250px;
  left: 120px;

  width: 130px;
}

#box-3 {
  top: 268px;
  left: 120px;

  width: 130px;
}

#box-4 {
  top: 304px;
  left: 120px;

  width: 100px;
}

#box-5 {
  top: 340px;
  left: 120px;

  height: 56px;
  width: 186px;
}

.slidev-vclick-hidden {
  block-size: 0;
}

</style>

---

# 文字列は文字の列

- 演習問題
  - https://atcoder.jp/contests/abc062/tasks/abc062_b
