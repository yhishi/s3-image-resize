# S3 × lamda × CloudFormation

### 概要
* S3バケットに挙がっている画像のリサイズ
* 指定のバケットにオブジェクトが作られると、lamdaが動きアウトプット用のバケットにリサイズした画像が出力される

### コマンド
* デプロイ
`serverless deploy`

* リージョン間でまとめてオブジェクトの移動
`aws s3 sync s3://[バケットA]/ s3://[バケットB]/ --source-region [バケットAリージョン] --region [バケットBリージョン] --acl public-read`

### 参考サイト
https://blog.serverworks.co.jp/tech/2016/10/19/serverless_framework/