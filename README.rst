これは何？
=========

`cakespa.org <http://cakespa.org>`_ で公開されているドキュメントです。
これらのドキュメントは全て、 `Sphinx <http://sphinx.pocoo.org/>`_ を使って管理されています。


貢献する
========

以下の手順でこのドキュメントに貢献できます。

#. このリポジトリをフォークする。
#. 下記に定めるルールに従って、ドキュメントを記載する。
#. プルリクエストを送る。
#. このリポジトリの管理者が修正し、変更を取り入れる。
#. `cakespa.org <http://cakespa.org>`_ に反映される。


ドキュメントに関するルール
==========================

ドキュメントを書く際は下記のルールに従ってください。

* page.rst.exampleを参考にドキュメントを作成する。
* ドキュメントはdocumentsディレクトリ以下に配置する。
* 1ページで終わる記事は、ディレクトリを作成しない。
* 複数ページに渡る記事は、documentsディレクトリのルートにトップページを作成する。その他のページはトップページと同名のディレクトリを作成し、その中に配置する。
* 画像は_staticディレクトリに配置する。内部のディレクトリは、ドキュメントと同じ構成で配置する。


ドキュメントで使用するマークアップ
====================================

reStructuredTextを使用します。
下記のページを参考に、ドキュメントを書いてください。

* `reStructuredText入門 <http://sphinx-users.jp/doc10/rest.html>`_


自分でビルドする
================

自分でビルドするためには、Sphinxのインストールが必要です。
以下の記事を参考に、Sphinxをインストールしてください。

* `Pythonって何？という人のためのSphinxインストール入門 <http://blog.shibu.jp/article/32044108.html>`_

| UbuntuやDebianをお使いの方は、apt-get installでなく、easy_installを使った方法をお勧めします。
| UbuntuやDebianで管理されているSphinxのパッケージは、バージョンが古いためです。

インストール後は下記のコマンドで、ビルド出来ます。

| make html


CentOS/FedoraにSphinxをインストールする
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

# yum install python-setuptools
# easy_install -U Sphinx


UbuntuにSphinxをインストールする
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

# apt-get install -y python-setuptools
# easy_install -U Sphinx


WindowsにSphinxをインストールする
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* `Windowsへのインストール <http://sphinx-users.jp/gettingstarted/install_windows.html#install-easy-install>`_


MacOSにSphinxをインストールする
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

# Xcodeをインストールする ( `Download Xcode <http://developer.apple.com/technologies/xcode.html>`_ )
# curl -O http://peak.telecommunity.com/dist/ez_setup.py
# sudo python ez_setup.py
# sudo easy_install sphinx
