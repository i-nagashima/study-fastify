# Plugins

Fastify は、ユーザーがプラグインでその機能性を拡張することを可能にします。プラグインは、ルートのセットやサーバーデコレーターなど、何でもかまいません。1 つまたは複数のプラグインを使用するために必要な API は、登録されています。

デフォルトでは、register は新しいスコープを作成します。これは、Fastify インスタンスに何らかの変更を加えた場合（decorate を介して）、この変更は現在のコンテキストの祖先には反映されず、その息子にのみ反映されることを意味します。この機能により、プラグインのカプセル化と継承を実現することができます。このようにして、DAG（Direct Acyclic Graph）を作成し、クロスディペンデンシーによる問題が発生しないようにします。

この API の使い方は非常に簡単であることは、「はじめに」のセクションですでに説明したとおりです。