# よくつかうPythonのプログラミング

## 文字を出す

```python
print("Hello")
print("こんにちは")
```

## 計算する

```python
a = 5
b = 3
print("足し算の結果:", a + b)
print("引き算の結果:", a - b)
print("掛け算の結果:", a * b)
print("割り算の結果:", a / b)
```

## 入力させる

```python
name = input("名前を入力してください: ")
print("こんにちは、" + name + "さん！")
age = input("年齢を入力してください: ")
print("あなたは" + age + "歳ですね。")
```

## 条件分岐

```python
age = 30

if score >= 70:
    print("おじいちゃんですね")
elif score >= 40:
    print("おじさんですね")
else:
    print("おにいちゃんですね")
```

## 繰り返し

```python
for i in range(1, 5):
    print(str(i) + "回目のこんにちは。")
```

## 文字を数字に変換する

```python
num = int("123")
print("文字を数字に変換:", num)
```

## 数字を文字に変換する

```python
num_str = str(456)
print("数字を文字に変換:", num_str)
```

## リスト・配列

```python
fruits = ["りんご", "バナナ", "みかん", "ぶどう"]
print(fruits[0])
print(fruits[1])
print(fruits[3])

for fruit in fruits:
    print(fruit + "が好きですか？")
```

## 関数

```python
def hello(name):
    print(name + "さん、こんにちは！")

hello("太郎")
hello("花子")
```

## 【モジュール(拡張機能)】おしゃれな文字をだす『pyfiglet』

インストール
```bash
pip install pyfiglet
```

使い方
```python
import pyfiglet   # モジュール読み込み

print(pyfiglet.figlet_format("Hello"))
print(pyfiglet.figlet_format("Hello", font="slant"))
```

## 【モジュール(拡張機能)】図形を描く『turtle』

使い方
```python
import turtle       # モジュール読み込み

t = turtle.Turtle() # Turtleを作成
t.shape("turtle")   # かたち
t.color("orange")   # 色

# 4角形
for _ in range(4):  # 4回くりかえす
    t.forward(100)  # 100歩進む
    t.right(90)     # 90度まわす

turtle.done()       # おわり
```

## 【モジュール(拡張機能)】Webサイトをつくる『Flask』

インストール
```bash
pip install flask
```

使い方
```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def index():
    return "Hello"

@app.route("/sample")
def sample():
    return "Sample"

app.run()
```

使い方（HTMLを読み込むとき）
```python
from flask import Flask
from flask render_template

app = Flask(__name__)

@app.route("/")
def index():
    return render_template("index.html")

@app.route("/sample")
def sample():
    return render_template("sample.html")

app.run()
```
※ 「templates」というフォルダの下に「index.html」と「sample.html」を置いています
