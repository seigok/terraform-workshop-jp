# Terraform 基礎ブロック（初学者向け 60〜90 分）

この章は、後続の Cloud / Enterprise 章に入る前に、Terraform CLI の基本サイクルを短時間で体験するための導入です。

## この章のゴール

- `init / fmt / validate / plan / apply / destroy` の最小ループを 1 回完了する
- `terraform.tfstate` が何を保持するかを理解する
- `plan` の差分を読んで、`apply` 前に変更内容を判断できる状態になる

## 事前準備

- Terraform CLI がインストール済み
- 動作確認: `terraform version`
- 任意の作業ディレクトリを作成済み

## 1. 最小構成を作る

`main.tf` を作成します。

```hcl
terraform {
  required_version = ">= 1.5.0"
}

resource "null_resource" "example" {}
```

## 2. CLI の基本サイクルを実行する

```bash
terraform init
terraform fmt
terraform validate
terraform plan
terraform apply -auto-approve
terraform destroy -auto-approve
```

## 3. state を確認する

`apply` 後に `terraform.tfstate` が生成されます。

- state は「Terraform が管理している実体の現在状態」を保持するファイルです
- team 運用では local state ではなく remote state（Terraform Cloud など）を利用します

確認コマンド例:

```bash
terraform show
terraform state list
```

## 4. 次の章へ

基礎が完了したら、次に [Terraform Cloud によるリモートステート管理](./tfc-remote-state.md) へ進みます。

## 完了条件

- 上記 6 コマンドをエラーなく実行できた
- `terraform.tfstate` の役割を説明できる
- `plan` の出力から「何が変わるか」を口頭で説明できる
