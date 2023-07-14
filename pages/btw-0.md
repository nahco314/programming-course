# ブロックとスコープ

<v-clicks>

- ブロック: {} で囲まれた文のかたまり
  - if や else の {}
  - if や else の {} を省略した場合でも、ブロックとなる
  - main関数を囲む {} に関しては多分扱いが違う

+ ブロックの中では**スコープ**が形成される
  + スコープ: 変数が使える範囲

- 変数は、それが宣言されたブロックの中でのみ使える

</v-clicks>

---

# ブロックとスコープ

- これらはコンパイルエラーとなる

<center>

```cpp
if (a < b) {
  string message = "a is big";
}
cout << message << endl;
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 24px  !important;
}
</style>

---

# ブロックとスコープ

- これらはコンパイルエラーとなる

<center>

```cpp
if (a < b) {
  string message = "a is big";
} else {
  message = "b is big";
}
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 24px  !important;
}
</style>

---

# ブロックとスコープ

- これらはコンパイルエラーとなる

<center>

```cpp
if (a < b) {
  string message = "a is big";
} else {
  string message = "b is big";
}
cout << message << endl;
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 24px  !important;
}
</style>

---

# ブロックとスコープ

- if や else と関係なく、スコープを作るためにブロックを作ることもできる

<center>

```cpp
int main() {
  int a = 3;
  
  {
    int n = 5;
    cout << a * n << endl;
  }
}
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 20px  !important;
}

</style>

---

# ブロックとスコープ

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_co​

---

# 複合代入演算子

- 特定の形の単純な更新は短縮して書ける

<center>

| 元の形          | 短縮形      |
|--------------|----------|
| `a = a + 5;` | `a += 5` |
| `n = 3 * n;` | `n *= 3` |
| `a += 1;`    | `a++;`   |
| `a -= 1;`    | `a--;`   |
| `a += 1;`    | `++a;`   |

</center>

<style>

table {
  margin-top: 20px;
  width: 600px;
}

</style>

---

# 複合代入演算子

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_cn

---

# 空白、改行、インデント

- 今までのコードにはたくさんの空白や改行が含まれていた
- が、実は空白や改行に意味は無い
  - 人間が読みやすくなるだけ

---

# 空白、改行、インデント

- これは:

```cpp
#include<bits/stdc++.h>
using namespace std;

int main() {
  int a = 3;

  int n = 5;
  cout << a * n << endl;
}
```

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 20px  !important;
}

</style>

---

# 空白、改行、インデント

- これと全く同じ意味:

```cpp
#include<bits/stdc++.h>
using namespace std;int main(){int a=3;int n=5;cout<<a*n<<endl;}
```

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 18px  !important;
}

</style>

---

# 空白、改行、インデント

- 行の始まりの連続した空白は**インデント**

<center>

```cpp
int main() {
  int n;
  cin >> n;
  
  if (n % 15 == 0) {
    cout << "FizzBuzz" << endl;
  } else {
    if (n % 3 == 0) {
      cout << "Fizz" << endl;
    } else {
      if (n % 5 == 0) {
        cout << "Buzz" << endl;
      } else {
        cout << n << endl;
      }
    }
  }
}
```

</center>

<div v-click class="box" id="box-0"></div>
<div v-click class="box" id="box-1"></div>
<div v-click class="box" id="box-2"></div>
<div v-click class="box" id="box-3"></div>
<div v-click class="box" id="box-4"></div>
<div v-click class="box" id="box-5"></div>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 11.5px  !important;
}

.box {
  border: none;
  width: 13px;
}

#box-0 {
  top: 310px;
  left: 125px;

  background-color: green;
  opacity: 0.5;
  height: 18px;
}

#box-1 {
  top: 344px;
  left: 125px;

  background-color: green;
  opacity: 0.5;
  height: 158px;
}

#box-2 {
  top: 360px;
  left: 138px;

  background-color: yellowgreen;
  opacity: 0.5;
  height: 20px;
}

#box-3 {
  top: 395px;
  left: 138px;

  background-color: yellowgreen;
  opacity: 0.5;
  height: 90px;
}

#box-4 {
  top: 412px;
  left: 151px;

  background-color: yellow;
  opacity: 0.5;
  height: 20px;
}

#box-5 {
  top: 447px;
  left: 151px;

  background-color: yellow;
  opacity: 0.5;
  height: 20px;
}

</style>

---

# 空白、改行、インデント

- これらは意味がないが、しっかりと書くことでバグを減らせる

+ ちゃんと書いたほうがいい
