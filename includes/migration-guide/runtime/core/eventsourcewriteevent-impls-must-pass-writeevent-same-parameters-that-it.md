### <a name="eventsourcewriteevent-impls-must-pass-writeevent-the-same-parameters-that-it-received-plus-id"></a>同じ受け取ったパラメーター (と ID)、EventSource.WriteEvent impls が WriteEvent を渡す必要があります。

|   |   |
|---|---|
|説明|ランタイムは次の内容を指定するコントラクトを強制するようになりました: ETW イベント メソッドを定義する <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> から派生するクラスは、ETW イベント メソッドが渡された同じ引数が続くイベント ID の基底クラス <code>EventSource.WriteEvent</code> メソッドを呼び出す必要があります。|
|提案される解決策|<xref:System.IndexOutOfRangeException?displayProperty=name> 例外は、<xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> がこのコントラクトに違反するイベント ソースのプロセスの <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> データを読み取るときに、スローされます。|
|スコープ|マイナー|
|Version|4.5.1|
|型|ランタイム|
