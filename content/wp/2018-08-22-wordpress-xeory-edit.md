---
title: WordPressの軽量化のためXeoryのソーシャルボタンを修正してみた
author: ひろたつ
type: post
date: 2018-08-22T14:02:56+00:00
url: /wordpress-xeory-edit/
thumbnail: 'images/uploads/2018/08/d199783a8706540ba26bc8e4fb6b0ade.png?fit=304%2C171&ssl=1'
views:
  - 437
bzb_meta_keywords:
  - xeory
bzb_meta_robots:
  - 'a:2:{i:0;s:0:"";i:1;s:0:"";}'
bzb_post_layout:
  - left-content
bzb_cta:
  - 'a:6:{s:9:"check_cta";s:4:"none";s:9:"org_title";s:0:"";s:9:"org_image";s:0:"";s:11:"org_content";s:0:"";s:15:"org_button_text";s:0:"";s:14:"org_button_url";s:0:"";}'
bzb_checklists:
  - 'a:1:{i:0;s:0:"";}'
categories:
  - WordPress
tags:
  - xeory
  - ソーシャルボタン

---
はいどーもー
  
エンジニアのひろたつです。

今回は、このブログで使用しているXeoryというテーマの改良です。
  
ソーシャルボタンが重すぎるので、修正して軽量化してみました。

<!--more-->

<div id="toc_container" class="toc_transparent no_bullets">
  <p class="toc_title">
    本記事の内容
  </p>
  
  <ul class="toc_list">
    <li>
      <a href="#i"><span class="toc_number toc_depth_1">1</span> はじめに</a>
    </li>
    <li>
      <a href="#snsphp"><span class="toc_number toc_depth_1">2</span> sns.phpの作成</a>
    </li>
    <li>
      <a href="#singlephp"><span class="toc_number toc_depth_1">3</span> single.phpの修正</a>
    </li>
    <li>
      <a href="#i-2"><span class="toc_number toc_depth_1">4</span> おわりに</a>
    </li>
    <li>
      <a href="#i-3"><span class="toc_number toc_depth_1">5</span> 参考</a>
    </li>
  </ul>
</div>

## <span id="i">はじめに</span>

わたくし、ひろたつはブログを運営しています。
  
その中でちょっとしたことなのですが、悩みが、、
  
いかんせん、ソーシャルボタンの表示がおそい！
  
本当に遅い！！
  
調べると、画像を取得するのに時間がかかっているのだとか、、、
  
そんなのしなくていいよ〜〜〜

と、いうわけで、画像を読み込まないソーシャルボタンを自分で作って、それに変更しちゃいます。
  
これができたら、一瞬で表示されるブログが完成するぞ〜〜〜
  
いぇ〜〜い！

## <span id="snsphp">sns.phpの作成</span>

まずは、sns.phpというファイルを作成します！
  
僕はCUIで操作しているので、、

    touch sns.php
    

これで新しいファイルを作成します。

そして、そのファイルを修正します。

    vi sns.php
    



こんな感じです。
  
5行目あたりで勝手に、マージンを入れています。気になる方は、各自で修正してください。

margin-top: -30px;は上に余白がありすぎたので、入れました。
  
margin-bottom: 20px;は下に余白が全く無かったので入れました。

## <span id="singlephp">single.phpの修正</span>

sns.phpが完成したら、それを読み込まなくてはいけません。

というわけで、single.phpを修正していきます。

    vi single.php
    

と、いっても簡単です。

１．まずは、、、
  


上記の部分を見つけて削除します。(64行目あたりにあります。)

  1. 次に、、、
  
    削除したところに以下を追記します。



以上です。

これで先程作成したsns.phpが読み込まれて、表示されると思います。

ソーシャルボタンがいい感じになったのではないでしょうか〜

## <span id="i-2">おわりに</span>

簡単でしたよね〜
  
Xeoryテーマはシンプルで使いやすいですよね。

そして、なんか違うなって思う部分はどんどん修正して、自分色に染めていきましょう〜

以上、ひろたつでした。
  
ばいなら〜

## <span id="i-3">参考</span>

> <a href="https://soricity.com/social-button-change/" rel="noopener" target="_blank">https://soricity.com/social-button-change/</a> 

> <a href="https://sekkakudakara.com/share-buttons/" rel="noopener" target="_blank">https://sekkakudakara.com/share-buttons/</a> 

<div style="font-size: 0px; height: 0px; line-height: 0px; margin: 0; padding: 0; clear: both;">
</div>
