# 関数

- 関数: 処理をまとめたもの
- 数学の関数みたいな感じで書くので関数

<v-click>

+ 例を見てみよう

</v-click>

---
clicks: 4
---

# 関数

- 2つの整数 a,b のうち、小さい方を求めたい

<br>

<div v-click-hide="3">
<div v-click="1">

+ 普通に書くと...

</div>
</div>

<div v-click="3">

+ 関数を使って書くと...

</div>

<center>

<div v-click-hide="3">
<div v-click="2">

```cpp
int res;
if (a > b) {
  res = b;
} else {
  res = a;
}
```

</div>
</div>

<div v-click="4">

```cpp
int res = min(a, b);
```

</div>

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 20px  !important;
}

.slidev-vclick-hidden {
  block-size: 0;
}

</style>

---

# 関数

<center>

```cpp
int res = min(a, b);
```

</center>

- `min` という関数に、`a` と `b` を渡している

<v-clicks>

+ `min`: 2つの数の小さい方を**返す**関数
+ 関数に渡す値のことを、**引数**と呼ぶ
+ 関数の計算結果のことを**返り値**や**戻り値**と呼ぶ
+ 引数や返り値は型が決まっている

</v-clicks>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-bottom: 40px;
}

.slidev-code code {
  font-size: 20px  !important;
}

.slidev-vclick-hidden {
  block-size: 0;
}

</style>

---

# 関数

- C++ で用意されている、関数とかがまとまっているものを STL という
- min も STL に入っている関数

---

# 関数 - 便利なSTL関数

<v-clicks>

- `min(a, b)`: a と b のうち小さい方を返す
- `max(a, b)`: a と b のうち大きい方を返す
- `swap(a, b)`: a と b の値を交換する(a と b は変数などを渡す)
- 他にもたくさん

</v-clicks>

---

# 関数

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_ci

---

# 関数定義

- 関数を自分で**定義**することもできる
  - 定義: 関数を作ること

<center>

```cpp
返り値の型 関数名(引数1の型 引数1の名前, 引数2の型 引数2の名前, ...) {
  処理
}
```

</center>

- `return 返り値;` と書くことで値を返す

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 40px;
  margin-bottom: 25px;
}

.slidev-code code {
  font-size: 20px  !important;
}

.slidev-vclick-hidden {
  block-size: 0;
}

</style>

---
clicks: 3
---

# 関数定義 - 例 1

<center>

```cpp
int my_min(int a, int b) {
  if (a > b) {
    return b;
  } else {
    return a;
  }
}
```

</center>

<div v-click-hide="2"><div v-click="1">

- 2 つの `int` 型の引数を取り、`int` 型を返す `my_min` という関数

</div></div>

<div v-click-hide="3"><div v-click="2">

- `a` と `b` のうち小さい方を return している

</div></div>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 40px;
  margin-bottom: 25px;
}

.slidev-code code {
  font-size: 24px  !important;
}

.slidev-vclick-hidden {
  block-size: 0;
}

</style>

---
clicks: 5
---

# 関数定義 - 例 2

<center>

```cpp
void hello(string name) {
  cout << "Hello," << name << "!" << endl;
}
```

</center>

<div v-click-hide="3">
<div v-click="1">

- `void` ってなに？

</div>
<div v-click="2">

- →「返り値が無い」ことを表す

</div>

</div>

<div v-click-hide="4"><div v-click="3">

- `string` を受け取り、何も返さない関数

</div></div>

<div v-click-hide="5"><div v-click="4">

- 処理内容は出力

</div></div>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 40px;
  margin-bottom: 40px;
}

.slidev-code code {
  font-size: 24px  !important;
}

.slidev-vclick-hidden {
  block-size: 0;
}

</style>

---
clicks: 3
---

# 関数定義 - 例 3

<center>

```cpp
int two_div_count(int n) {
  int res = 0;
  while (true) {
    if (n % 2 != 0) {
      return res;
    }
    n /= 2;
    res++;
  }
}
```

</center>

<div v-click-hide="2"><div v-click="1">

- 引数 n が何回 2 で割れるかを返す関数

</div></div>

<div v-click-hide="3"><div v-click="2">

- return 文は、「関数の処理を終了させ、値を返す」という挙動

</div></div>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 40px;
  margin-bottom: 25px;
}

.slidev-code code {
  font-size: 18px  !important;
}

.slidev-vclick-hidden {
  block-size: 0;
}

</style>

---
clicks: 9
---

# 関数定義 - 実行の流れ

<center>

```cpp
int my_min(int a, int b) {
  if (a > b) {
    return b;
  } else {
    return a;
  }
}

int main() {
  cout << my_min(3, 10) << endl;
}
```

</center>

<div v-click-hide="2"><div v-click="1">

- main 関数が実行される

</div></div>

<div v-click-hide="3"><div v-click="2">

- main 関数の 1 行目の出力が実行される

</div></div>

<div v-click-hide="4"><div v-click="3">

- `my_min(3, 10)` が評価され、`my_min` 関数が実行される

</div></div>

<div v-click-hide="5"><div v-click="4">

- if が実行される

</div></div>

<div v-click-hide="6"><div v-click="5">

- `a > b` は偽なので、else の方が実行される

</div></div>

<div v-click-hide="8"><div v-click="6">

- `a` が返され、関数内での処理が終了する

</div></div>

<div v-click-hide="9"><div v-click="8">

- 3 が出力される

</div></div>

<div v-click-hide="2"><div v-click="1" class="box" id="box-0"></div></div>
<div v-click-hide="3"><div v-click="2" class="box" id="box-1"></div></div>
<div v-click-hide="4"><div v-click="3" class="box" id="box-2"></div></div>
<div v-click-hide="4"><div v-click="3" class="box" id="box-3"></div></div>
<div v-click-hide="6"><div v-click="4" class="box" id="box-4"></div></div>
<div v-click-hide="7"><div v-click="6" class="box" id="box-5"></div></div>
<div v-click-hide="8"><div v-click="7" class="box" id="box-2"></div></div>
<div v-click-hide="9"><div v-click="8" class="box" id="box-1"></div></div>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 40px;
  margin-bottom: 10px;
}

.slidev-code code {
  font-size: 18px  !important;
}

.box {
  height: 24px;
}

#box-0 {
  height: 85px;
  width: 355px;

  top: 376px;
  left: 104px;
  
  border-color: red;
}

#box-1 {
  width: 333px;

  top: 406px;
  left: 126px;
  
  border-color: orange;
}

#box-2 {
  width: 147px;

  top: 406px;
  left: 213px;
  
  border-color: orange;
}

#box-3 {
  height: 192px;
  width: 292px;

  top: 161px;
  left: 104px;
  
  border-color: orange;
}

#box-4 {
  height: 136px;
  width: 140px;

  top: 188px;
  left: 126px;
  
  border-color: blue;
}

#box-5 {
  width: 104px;

  top: 271px;
  left: 148px;
  
  border-color: blue;
}

.slidev-vclick-hidden {
  block-size: 0;
}

</style>

---

# 関数定義

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_ch
