# robosys_Kadai1_2
This is a repository for robosys Kadai1 version 2.

# このリポジトリについて
　robosys_Kadai1のリポジトリを作成していましたが、上手く作成することができなかった箇所があったので、二つ目のものを作成しました。そのため、[robosys_Kadai1](https://github.com/ryunosukesato/robosys_Kadai1)のリポジトリの訂正版となっています。それに伴い、このREADMEは私のrobosys_Kadai1のリポジトリの作成途中のREADMEからコピーアンドペーストした部分が大半になっています。

# License（ライセンス）
GPL-2.0 License

# Author（著者）
## Ryuichi Ueda
（下記の参考ビデオの『ロボットシステム学第7回～第8回』をみながら、著者が作成したコードと同じコードを私が記入しただけなので、コードの著作権は著者にあります。ただし、コード最上部2行のコメントアウトしている部分は、『ロボットシステム学第9回（ソフトウェアライセンスとクリエイティブ・コモンズ）』（49分15秒あたり）を参考にして、『ロボットシステム学第7回～第8回』で著者が作成したコードに私が追記したものです）

# どんなデバイスドライバか
　このリポジトリに掲載してあるデバイスドライバはLEDを点灯・消灯するものです。  

## 使用する（した）もの・機器
・ラズベリーパイ4 (Ubuntu 20.04.3 LTS)  
・ブレッドボード  
・ジャンパケーブル（オス-メス） 2個  
・LED  
・抵抗（300Ω）橙黒茶金  

## 回路図
・ラズパイ4のGPIO25（22番ピン）とGND（39番ピン）の間にLEDと抵抗を接続  
※LEDのアノード（足の長い方）をGPIO25に接続すること  
[回路図](./%E8%AA%B2%E9%A1%8C1.jpg)

# インストール方法
GitHubからこのリポジトリをcloneした後、下記の順に従って入力することでLEDを点灯・消灯させる事ができます。  
ls  
cd robosys_Kadai1_2/  
ls  
make  
sudo insmod myled.ko  
sudo chmod 666 /dev/myled0  

LEDを点灯するためには  
echo 1 > /dev/myled0　と入力し  
LEDを消灯するためには  
echo 0 > /dev/myled0　と入力してください


# 参考
## 参考ビデオ(YouTube)
講義動画のためURLは掲載しない

Git, GitHubについて  
・ロボットシステム学第3回補足（GitHubへの鍵の登録）  
・ロボットシステム学第3回（GitとGitHub）

コードについて  
・ロボットシステム学第7回～第8回  
・ロボットシステム学第9回（ソフトウェアライセンスとクリエイティブ・コモンズ）

## GitHubの扱い方について  
・[ファイルの名前を変更する - GitHub Docs](https://docs.github.com/ja/repositories/working-with-files/managing-files/renaming-a-file)  
・[GitHub — READMEの作成方法と書き方【改行やリンク・画像の入れ方】| Howpon[ハウポン]](https://howpon.com/8334)  
・pushの仕方をお教えいただいたyuzukiimaiさんのリポジトリは[こちら](https://github.com/yuzukiimai/robosys1)になります。  
### 【yuzukiimaiさんにお教えいただいた経緯と手順について】  
robosys_Kadai1のリポジトリに修正したコードをpushする際、GitHubに上手くpushできないという事態が発生したため、yuzukiimaiさんにpushの仕方をお教えいただきました。yuzukiimaiさんにお教えいただいていた手順を示すURLは以下のものです。  
・[(Git) git init ~ git push で詰まった話。めっちゃrejectされる | hara-chan.com](https://hara-chan.com/it/programming/git-push-rejected/)


### READMEについて
・どのように書けば良いかの参考として、コードの著者[Ryuichi Ueda](https://github.com/ryuichiueda)のREADMEをいくつか拝見し、このREADMEを書きました  
・何を書いたのかを話した友人のリポジトリは [こちら](https://github.com/NagashimaKousei/robosys_1)になります  
### 【READMEについて友人と話した経緯】  
課題の一回目の提出終了後、その友人と「どんなこと書いた？」というような会話になり、使用する（した）もの・機器を、私は一回目の提出時までに書いていなかったので、その友人の言葉を参考にし、記載しました。


## 必要となる道具とその扱い方について
・[【ラズパイ電子工作】LEDを点灯させる方法(GPIO使用)| 電気設計人.com](https://denkisekkeijin.com/raspberrypi/pi-led/)  
・[Raspberry PiでLEDの点灯 - Quita](https://qiita.com/aryoa/items/3f6d82b8c63761cef087)  
・[ブレッドボードの使い方 | Spiceman](https://spiceman.jp/bread-board/)  
