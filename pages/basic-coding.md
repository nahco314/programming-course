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

# 出力

<center>

```cpp
int main() {
    cout << "Hello,World!" << endl;
}
```

</center>

<div id="cout-box">
<h3><span>cout</span></h3>
<div class="inner">

<div v-click="1">
Hello,World!
</div>

<div v-click="2">
<br>
</div>

</div>
</div>

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
#cout-box span{
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

</style>

---

# 出力

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

<div v-click="4" v-click-hide="5" class="br-div">
&nbsp;
</div>

<div v-click="5">
1234
</div>

<div v-click="6">
&nbsp;
</div>

</div>
</div>

<style>

.slidev-code code {
  font-size: 16px  !important;
}

pre[class*='language-'] {
  width: 900px;
  margin-bottom: 40px;
}

#cout-box {
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

:not(.slidev-vclick-prior, .slidev-vclick-current).br-div {
  block-size: 0;
}

</style>

---

# 出力

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_cv
