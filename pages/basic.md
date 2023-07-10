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

# コードの構造

- 文: コンピュータに対する1つの命令
- C++ のコードは、文を並べて記述する
- コンピュータは並べられた文を順に実行していく

+ 文の命令内容は例えば…
  <ul>
    <li v-click>「この式を計算して」</li>
    <li v-click>「これを出力して」</li>
    <li v-click>「もしも〜ならこの文を実行して」</li>
    <li v-after>とか</li>
  </ul>

---

# コードの構造

- 詳しくは後述するが、C++ では文の区切りとして、全ての文の末尾に `;` をつける
- これを忘れるとエラーになるので気をつけよう

+ `;` はセミコロンと読む　日本語キーボードでは「L」の右

---

# コメント

- コードの中には、コメント(注釈)を書くことができる
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
  
  x = 8;  // おわり
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
