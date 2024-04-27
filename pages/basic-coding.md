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

<!--
整数型の値を表現する単純な式として整数リテラルがあって、というのが正確ではあるが、それは難しいのでまず数を書けるというゆるふわな理解から出発する
-->

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

<!--
ここも、C++における式という概念をしっかり理解させるより前に、なんとなく四則演算が書けるということを言う
-->

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

---

# 四則演算 - 小数

- 小数を扱うこともできる

<center>

```cpp
int main() {
  cout << 1.0 + 2.5 << endl;  //  3.5
  cout << 5 * 0.25 << endl;   //  1.25
  cout << -2.0 - 0.4 << endl; // -2.4
}
```

</center>

<style>

.slidev-code code {
  font-size: 24px  !important;
}

pre[class*='language-'] {
  width: 650px;
  margin-top: calc(30px + 43.2px);
}

</style>

<!--
ここも同じように、intやfloatの概念よりも前に、整数や小数が扱える、というゆるふわな説明で行く
-->

---

# 四則演算 - 小数

- 整数同士の割り算は切り捨てだが、割る数か割られる数のどちらかが小数なら結果は小数になる

<center>

```cpp
int main() {
  cout << 7 / 3 << endl;      // 2
  cout << 7.0 / 3 << endl;    // 2.33333
  cout << 7 / 3.0 << endl;    // 2.33333
  cout << 7.0 / 3.0 << endl;  // 2.33333
}
```

</center>

<style>

.slidev-code code {
  font-size: 24px  !important;
}

pre[class*='language-'] {
  width: 650px;
  margin-top: 30px;
}

</style>

---

# 四則演算

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_ct
