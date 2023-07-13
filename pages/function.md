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
