# Encored Japan Python Common Helper Library


## パッケージ作成

`setup.py` は `setuptools` を使う。Python 3.12 以降（Homebrew の Python 3.13 を含む）には同梱されていない。未インストールのまま実行すると次のエラーで止まる。

```text
ModuleNotFoundError: No module named 'setuptools'
```

Homebrew の Python はシステム管理下のため、先にユーザー領域へ `setuptools` を入れてからソース配布を作る。

```bash
python3.13 -m pip install --user --break-system-packages setuptools
python3.13 setup.py sdist
```

成果物は `dist/ejhelper-<version>.tar.gz`。ライセンス分類子の警告が出ても、アーカイブの作成は完了している。
