# graphrag-hackathon

## インストール

```
$ git clone https://github.com/teshi22/graphrag-hackathon.git
$ cd graphrag-hackathon
$ python -m venv .venv
$ source .venv/bin/activate
$ pip install -r requirements.txt
$ ipython kernel install --user --name=graphrag-hackathon-env
```

## プロジェクトの初期化

```
$ mkdir ex1
$ graphrag init --root ./ex1
```

## .env 作成

```
$ cd ex1
$ vi .env
```

```
GRAPHRAG_API_KEY=<api-key>
```

## データ配置

./ex1/input に内にデータを配置

## インデックス作成

```
$ graphrag index --root ./ex1
```

## プロンプトチューニング

```
graphrag prompt-tune --root ./ex1 --output ./ex1/tuned_prompts
```

## クエリ

```
$ graphrag query --root ./ex1 --method global --query "Azure OpenAIで使えるモデルを教えて"
$ graphrag query --root ./ex1 --method local --query "Azure OpenAIで使えるモデルを教えて"
```
