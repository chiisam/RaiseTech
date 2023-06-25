# 第4回課題

## VPC設定
![sampleap](img/Lecture04_vpc_setting.png)
- 追加分
![sampleap](img/Lecture04_vpc_subnet.png)

## EC2設定
![sampleap](img/Lecture04_ec2_setting.png)
- 追加分
![sampleap](img/Lecture04_ec2_secgroup.png)

## RDS設定
![sampleap](img/Lecture04_rds_setting.png)
- 追加分
![sampleap](img/Lecture04_rds_secgroup.png)

## EC2からRDSへ接続
![sampleap](img/Lecture04_ec2-mysql_connect.png)

## メモ
- EC2を違うVPCで作ってしまい、それに気づくのに時間がかかった。
- DBにつなげようとしたところ以下のエラーが出てきてしまい、
- セキュリティグループの見直しで時間がかかった。
- ERROR 2003 (HY000): Can't connect to MySQL server on 'database-1.c37ertscx9vr.ap-northeast-1.rds.amazonaws.com' (110)
- 何回もEC2を作り直し、その都度セキュリティグループを作成していたため、うまく接続できなかった。
とりあえず3つ分セキュリティグループ（インバウンド）に入れている
- DBに接続したところ「Welcome to the MariaDB monitor.」と出てきた。
- 調べたところ、MariaDBに標準で搭載されているコマンドラインツール。
- なぜそれがMariaDB monitorが出てくるかは不明。
- プロンプトにはMySQL [(none)]>と出てきているので、とりあえずは気にせず進める。
