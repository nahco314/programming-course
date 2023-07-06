<style>

:root {
  --code-font-size: 24px  !important;
}

pre[class*='language-'] {
  width: 800px;
}

.sec-1 {
  display: flex;
  align-items: center;

  position: absolute;
  top: 170px;
  left: 100px;
}

.red-box {
  width: 375px;
  height: 80px;
  background-color: rgba(255, 0, 0, 0.25);
  border: 2px solid red;

  margin-right: 20px;
}

.sec-2 {
  display: flex;
  align-items: center;

  position: absolute;
  top: 280px;
  left: 100px;
}

.blue-box {
  width: 375px;
  height: 110px;
  background-color: rgba(0, 0, 255, 0.25);
  border: 2px solid blue;

  margin-right: 20px;
}

</style>

# コードの基本形

<div class="center">

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
  // ここにコードを書いていく
}
```

<div v-click class="sec-1">
<div class="red-box"></div>

← 必ず必要な「おまじない」

</div>


<div v-click class="sec-2">
<div class="blue-box"></div>

←&nbsp;

<div align="left">
main 関数、本質

この中身が実行される
</div>

</div>

</div>

---
