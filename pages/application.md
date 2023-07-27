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
+ たくさんコードを書いているうちに慣れていくと思うので頑張ろう

---

# 多次元配列

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_ce

---

# 再帰関数

## WIP
