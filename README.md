# add_lib_to_templ

## これはなに

競技プログラミングなどのライブラリをlineディテクティブを付けて一つのファイルにします。

## Usage

```
-add_lib_to_templ
  |-LICENSE
  |-README.md
  |-rend.py
  |-template.cpp.j2
  |-あなたのC++ライブラリ（ディレクトリ）
```

上のようなディレクトリ構造にします。

`$ pip install Jinja2 `

をした後

`$ python rend.py`

とすると`add_lib_to_templ`内にライブラリの中身が入ったcppファイルが出来上がります（デフォルトの名前が`template.cpp`になっています）。

ちなみに、`template.cpp.j2`の`{% for file in files_data %}`の前と`{% endfor %}`の後は編集して大丈夫です。お好みのテンプレートを作ってみてください。

## Option

### `-o`

レンダリングされたC++プログラムを保存するファイルの名前を指定します。デフォルト値は`template.cpp`です。

`$ python rend.py -o mytmp.cpp`

### `--encode`

ファイルの読み込み、書き込みを行うときの文字コードを指定します。デフォルト値は`utf-8`です。

`$ python rend.py --encord utf-16`

