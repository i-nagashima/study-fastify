# Decorators

デコレータ API は、サーバー インスタンス自体や、HTTP リクエスト ライフサイクル中に使用されるリクエストおよびリプライ オブジェクトなど、Fastify のコア オブジェクトのカスタマイズを可能にします。デコレータ API は、関数、プレーン オブジェクト、またはネイティブ タイプなど、あらゆるタイプのプロパティをコア オブジェクトにアタッチするために使用できます。

この API は同期的です。デコレーションを非同期に定義しようとすると、デコレーションが初期化を完了する前に Fastify インスタンスが起動してしまう可能性があります。この問題を回避し、非同期のデコレーションを登録するには、代わりに fastify-plugin と組み合わせた register API を使用する必要があります。詳細については、プラグインのドキュメントを参照してください。

この API でコアオブジェクトを装飾することで、基盤となる JavaScript エンジンは、サーバー、リクエスト、およびリプライオブジェクトの処理を最適化することができます。これは、インスタンス化されて使用される前に、すべてのオブジェクトインスタンスの形状を定義することで実現されています。例として、以下のようにすると、ライフサイクル中にオブジェクトの形状が変化してしまうため、推奨できません。