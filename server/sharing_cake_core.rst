:author: Takahiro Fujiwara
:created: 2011-01-22
:modified: 2011-01-22
:cakephp: 1.2, 1.3

CakePHPのコアコードを共有で使用するには
=======================================

ドキュメントにはありませんが、CakePHPではコアコードを複数のアプリケーション間で共有することが出来ます。
この方法を使うと、1サーバでCakePHPのコアコードを共通化でき、バージョン管理の煩雑さから解放されます。

やり方は簡単です。
webroot/index.php内の1行を修正するだけです。::

    <?php
    /**
     * The absolute path to the "cake" directory, WITHOUT a trailing DS.
     *
     */
        if (!defined('CAKE_CORE_INCLUDE_PATH')) {
            define('CAKE_CORE_INCLUDE_PATH', ROOT);
        }

CakePHPのコアコードの在り処は、このCAKE_CORE_INCLUE_PATH定数で決まります。
これをあなたの好きに書き換えましょう。
それだけです。::

    <?php
    /**
     * The absolute path to the "cake" directory, WITHOUT a trailing DS.
     *
     */
        if (!defined('CAKE_CORE_INCLUDE_PATH')) {
            define('CAKE_CORE_INCLUDE_PATH', DS . 'usr' . DS . 'lib' . DS . 'cakephp');
        }
