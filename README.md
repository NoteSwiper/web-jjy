# web-jjy

> **Note**
>
> this repository is fork from [`@shogo82148`]'s [`web-jjy`].

new features have included; 

**below document have original;**
---
電波時計の時刻合わせには、標準電波JJYと呼ばれる 時刻に関する情報を送信している電波が使われています。 
web-jjyは、この電波をブラウザ上で再現し、標準電波が届かない環境でも電波時計の時刻合わせを可能にするWebアプリです。

## 使い方

[JJYシミュレータWeb版](http://shogo82148.github.io/web-jjy/)ですぐに試せるデモページを公開してます。
パソコンのイヤホンジャックにアンテナ(普通のイヤホンで十分です)を接続し、電波時計の近くに置きます。 
音量を最大にし、「Start」ボタンを押すと信号が送信されます。 電波時計を強制受信モードにし、時刻が設定されるのを待ちましょう。

このページではパソコン自体の時刻を調整する機能はないので、 事前にNTPでパソコン自体の時刻設定を行っておくといいと思います。

## 免責事項

※ 利用の結果生じた損害について、一切責任を負いません。

## 動作環境

MacBook Air + Google Chrome 48.0.2564.116 + CITIZEN 8RZ152 で動作を確認しています。

## 原理

標準電波は40kHzまたは60kHzの電波です。 
電気が流れればそこには必ず電波が発生するので、イヤホンにこの周波数の信号を音声として流せば、
それだけで立派なアンテナになります。

ただし、一般的な音声アンプは人間の可聴域である20kHz以上の周波数の再生には適していません。
そこで、歪んだ波形に含まれる高調波を利用します。
ボリュームを大きくして音が割れた状態になると、音声信号は矩形波に近いかたちになります。 
13.333kHzの矩形波にはその3倍の39.999kHzの周波数成分が含まれるので、約40kHzの電波が出せるというわけです。 
詳しくは[フリーソフト電波時計用JJYシミュレータのページ](http://www.starstonesoft.com/jjy_simulator.htm)を参照してください。

## ライセンス

MITライセンスで提供します。[LICENSE.md](https://github.com/shogo82148/web-jjy/blob/gh-pages/LICENSE.md)を参照してください。

## 関連リンク

- [shogo82148/web-jjy](https://github.com/shogo82148/web-jjy)
- [Webブラウザを使って電波を出してみた](https://shogo82148.github.io/blog/2016/03/29/web-jjy/)
- [Web JJY が夏時間に対応しました](https://shogo82148.github.io/blog/2018/08/11/web-jjy-summer-time-support/)


[`@shogo82148`]: https://github.com/shogo82148
[`web-jjy`]: https://github.com/shogo82148/web-jjy
