# 課題
Mermaidを触ってみよう

マークダウンファイルを編集して、Mermaidで図を描いてみよう

# 取り組み方
* 本プロジェクトをforkしてください。
* README.mdを編集して、Mermaidを使いこなしてください
* できたらプルリクエストを出します

# 課題項目
## 流れ図
### 条件
- 開始と終了ノードをつける
- 条件分岐を組み込む
- 5ノード以上
- カッコいいほど高得点

## 解答
```mermaid
flowchart LR;
  A(["開始"]) --> B["値の入力"];
  B["値の入力"] --> C{"入力された値が負の値か？"};
  C{"入力された値が\n負の値か？"} --"負の値の場合"--> D["－１を掛ける"];
  C{"入力された値が\n負の値か？"} --"正の値の場合"--> F["入力された値の絶対値を表示"];
  D["－１を掛ける"] --> E["入力された値を表示"];
  E["入力された値を表示"] --> F["入力された値の絶対値を表示"]; 
  F["入力された値の絶対値を表示"] --> G(["終了"]);
```

## シーケンス図
### 条件
- 3人以上
- メッセージをやり取りしない人がいないように
- 自己呼び出しを含むこと
- カッコいいほど高得点

## 解答
```mermaid
sequenceDiagram
    actor 太郎
    actor 花子
    太郎->>花子: おはよう！
    activate 花子
    花子-->>太郎: おはようございます!
    deactivate 花子
```

## クラス図

### 条件
- 3つ以上
- 汎化と集約を含むこと
- カッコいいほど高得点

## 解答
```mermaid
classDiagram
    キャラクター o-- アイテム
```
