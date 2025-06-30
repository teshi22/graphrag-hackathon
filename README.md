# graphrag-hackathon

## 参考 URL

- https://microsoft.github.io/graphrag/

## ライブラリのインストール

graphrag のライブラリのインストールを行い、仮想環作成する

```
$ git clone https://github.com/teshi22/graphrag-hackathon.git
$ cd graphrag-hackathon
$ python -m venv .venv
$ source .venv/bin/activate
$ pip install -r requirements.txt
$ ipython kernel install --user --name=graphrag-hackathon-env
```

## プロジェクトの初期化

GraphRAG のプロジェクトを初期化する
(参考：https://microsoft.github.io/graphrag/get_started)

```
$ mkdir ex1
$ graphrag init --root ./ex1
```

## Azure OpenAI の API-KEY を設定

.env ファイルを編集する

```
$ cd ex1
$ vi .env
```

Azure OpenAI の API-KEY を設定する

```
GRAPHRAG_API_KEY=<api-key>
```

## データ配置

./ex1/input に内にデータを配置する
(参考：https://microsoft.github.io/graphrag/index/inputs/)

## インデックス作成

```
$ graphrag index --root ./ex1
```

## プロンプトチューニング

(参考：https://microsoft.github.io/graphrag/prompt_tuning/overview/)

```
graphrag prompt-tune --root ./ex1 --output ./ex1/tuned_prompts
```

## クエリ

(参考：https://microsoft.github.io/graphrag/query/overview/)

```
$ graphrag query --root ./ex1 --method global --query "Azure OpenAIで使えるモデルを教えて"
$ graphrag query --root ./ex1 --method local --query "Azure OpenAIで使えるモデルを教えて"
```
