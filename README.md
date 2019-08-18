# pythondiary

## 專案介紹
My frist website

## 成品展示
[網站位置(host by heroku)](https://python-diary.herokuapp.com)
![](https://github.com/Cgost/pythondiary/raw/master/index.png)

## 使用技術
工具名稱|用途
---|---
Python3 | 不需要解釋
Flask(python)    | 建立伺服器
HTML/CSS  | 網頁表示和排版
Heroku   | 託管網頁
Github   | 存放原始碼

## 片段程式碼
ˋˋˋpython
@app.route("/")
def home():
  temp = glob.glob("articles/*")
  fill = []
  for t in temp:
    category = t.replace("articles/", "")
    length = len(glob.glob(t + "/*.txt"))
    fill.append((category, length))
  return render_template("index.html", cat=fill)
  ˋˋˋ
