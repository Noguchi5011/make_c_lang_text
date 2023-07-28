# プログラム各行のエラー識別

## 仮想環境セットアップ

venvの場合
```
apt install python3-venv
python3 -m venv venv 
```

仮想環境の起動、モジュールのインストール
```
source ./venv/bin/activate
pip install -r requirements.txt
```

## 動作手順

.envファイルを作成し、api_keyの登録（必要な場合はプロキシ設定を記述）する。以下に例を示す。
exampleの箇所に実際のkeyを記述する。

.env
```
HTTP_PROXY=http://porxy:port
HTTPS_PROXY=https://porxy:port
api_key=example
```

登録を終えた後、以下の動作を行うことで、プログラム各行のエラーを`combined_results.json`として出力する。

```
source ./venv/bin/activate
bash run.sh 
```
