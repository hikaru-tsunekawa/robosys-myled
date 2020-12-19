## 内容
* 上記のプログラム等はRasberryPiを用いたデバイスドライバです．
* 以下の要件に従って実行するとLEDを点灯・点滅させることができます．

## 環境
* Rasberry Pi3 
* ubuntu20.04 lts

## 実行方法

* ラズパイのIPアドレスを取得(コマンドプロンプト等で`arp -a`を入力して検索等)して，ラズパイ環境内に入る
`$ ssh ubuntu@192.168.137.224  

* gitからコードをクローン
`$ git clone https://github.com//hikaru-tsunekawa/robosys-myled.git`

* makeしてコンパイル
`$ make`
`$ sudo insmod myled.ko`
`$ sudo chmod 666 /dev/myled0`

##　LED点灯

* LED点灯
   `$ echo 1 > /dev/myled0`
* LED消灯
   `$ echo 0 > /dev/myled0`
* LED 5回点灯
   `$ echo 2 > /dev/myled0`

## 後始末
```
$ sudo rmmod myled.ko
$ make clean
```

## 動画

## 参考文献
