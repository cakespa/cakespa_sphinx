モデルオブジェクトをどこでも呼び出すには
========================================

:author: Hiroki Shimizu
:created: 2011-02-20
:modified: 2011-02-20
:cakephp: 1.2, 1.3

単純にApp::import()を使ってからnewで初期化してもモデルオブジェクトは得られますが、ClassRegistry::init()を用いることを習慣付けましょう。::

	<?php
		$model = ClassRegistry::init('YourModelName'); 
	?>

簡単ですね。プラグインのモデルの呼び出し方は以下の通りです。::

	<?php
		$model = ClassRegistry::init('YourPlugin.YourModelName');
	?>

とっても簡単ですね！

ClassRegistryを使うと、インスタンスを複数生成してしまうことを避けることができます。
また、テストでは自動的にテスト用のDB設定を用いてくれるようになります。便利ですね！
