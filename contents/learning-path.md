# 学習レーンガイド（初学者 / 実務）

ワークショップの受講者レベルに応じて、以下の 2 レーンで進行できます。

## レーンA: 初学者レーン（Terraform OSS中心）

Terraform に初めて触れる参加者向けです。

### 推奨順序
1. [初めての Terraform](./hello-terraform.md)
2. [Terraform Cloud によるリモートステート管理](./tfc-remote-state.md)
3. [Secure Variable Storage](./variables.md)

### 到達目標
- `plan/apply/destroy` を一通り実行できる
- state と remote state の違いを説明できる
- 機密変数の扱い（mask / sensitive）を理解している

## レーンB: 実務レーン（Cloud / Enterprise中心）

Terraform の基本操作を理解済みで、運用設計や組織利用を学びたい参加者向けです。

### 推奨順序
1. [VCS 連携 (GitHub)](./vcs.md)
2. [VCS 連携 (Azure DevOps)](./vcs-azure.md)
3. [Enterprise 機能 1: RBAC](./teams.md)
4. [Enterprise 機能 2: Private Module Registry](./module.md)
5. [Enterprise 機能 3: Terraform Enterprise API](./tf-api.md)
6. [Enterprise 機能 4: Notifications](./notifications.md)
7. [API Drive Run](./api-driven-run.md)

### 到達目標
- チーム運用に必要な権限設計を説明できる
- モジュール再利用とバージョニング運用ができる
- API を使った Run の自動化フローを構築できる

## 運営向けメモ

- 参加者の自己申告スキルでレーンを分ける
- レーンA完了者がレーンBへ合流する進行も可能
- 1セッションで混在する場合は、共通パート（state / variables）を先に実施すると進行が安定する
