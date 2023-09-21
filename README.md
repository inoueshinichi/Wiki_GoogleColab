# Wiki_GoogleColab

## 参考
+ OS, GPUのバージョン https://wasurenamemo.blogspot.com/2020/09/google-colabosgpu.html
+ Google Colabの制限と対策 https://note.com/npaka/n/n1aa6f8c973d0

### Colabのセル上でコマンドを実行する場合`!`が必要
`!{command} {your arguments}`

### 主要情報確認コマンド
+ OS `$ uname -a`
+ GPU(Nvidia) `$ nvidia-smi`
+ Python `$ python --version`


### 90分ルール対策
+ Pythonスクリプトをローカル実行してColabのURLにアクセス
```
import time
import datetime
import webbrowser

# 1時間毎に任意のノートブックを開く
for i in range(12):
  browse = webbrowser.get('chrome')
  browse.open('<任意のノートブックURL>')
  print(i, datetime.datetime.today())
  time.sleep(60*60)
```
