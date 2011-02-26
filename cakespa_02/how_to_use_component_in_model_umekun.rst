componentをmodelで呼び出す方法（これはバッドプラクティスでしょうか？？）
+============
+
+:author: umekun123
+:created: 2011-02-24
+:modified: 2011-02-24
+:cakephp: 1.2, 1.3
+
+1.コンポーネントをフォルダにいれて、コントローラで指定
+public $components = array('Qdmail');
+
+2.モデルにファンクションを作成しておく
+public function setQdmailInModel($qdmail) {
+	$this->Qdmail = $qdmail;
+}
+
+3.コントローラで指定
+function useComponentInModel() {
+$this->Model->setQdmailInModel($this->Qdmail);
+$this->Model->sendEmail();
+}
+
+4.モデル内でコンポーネントを呼び出し
+$this->Qdmail->send();
