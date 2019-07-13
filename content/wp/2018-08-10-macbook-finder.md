---
title: MacbookのFinderの再起動をアプリにする
author: ひろたつ
type: post
date: 2018-08-09T19:08:55+00:00
url: /macbook-finder/
views:
  - 173
bzb_meta_keywords:
  - macbook
bzb_meta_robots:
  - 'a:2:{i:0;s:0:"";i:1;s:0:"";}'
bzb_post_layout:
  - left-content
bzb_cta:
  - 'a:6:{s:9:"check_cta";s:4:"none";s:9:"org_title";s:0:"";s:9:"org_image";s:0:"";s:11:"org_content";s:0:"";s:15:"org_button_text";s:0:"";s:14:"org_button_url";s:0:"";}'
bzb_checklists:
  - 'a:1:{i:0;s:0:"";}'
categories:
  - MacBook
tags:
  - Finder
  - macbook
  - スクリプトエディタ

---
はいどーもー
  
Finderの再起動コマンドをできるだけ簡単に実行したい欲求の強いひろたつです。

<!--more-->

今回の記事は、以前の続きみたいなものですｗ
  
↓↓↓
  
<a href="https://hirotatsu.me/howto-macbook/" rel="noopener" target="_blank">https://hirotatsu.me/2018/08/10/howto-macbook/</a>

<div id="toc_container" class="toc_transparent no_bullets">
  <p class="toc_title">
    本記事の内容
  </p>
  
  <ul class="toc_list">
    <li>
      <a href="#i"><span class="toc_number toc_depth_1">1</span> 何で作るの〜？</a>
    </li>
    <li>
      <a href="#i-2"><span class="toc_number toc_depth_1">2</span> 実際に作成していく</a>
    </li>
    <li>
      <a href="#i-3"><span class="toc_number toc_depth_1">3</span> 起動</a>
    </li>
    <li>
      <a href="#i-4"><span class="toc_number toc_depth_1">4</span> おまけ</a>
    </li>
    <li>
      <a href="#i-5"><span class="toc_number toc_depth_1">5</span> まとめ</a>
    </li>
    <li>
      <a href="#i-6"><span class="toc_number toc_depth_1">6</span> 参考</a>
    </li>
  </ul>
</div>

## <span id="i">何で作るの〜？</span>

Macbookで簡単なアプリケーションを作成できるって知ってましたか、？

実は、、、デフォルトでインストールされているアプリでMacbookで使えるアプリケーションを一瞬で作成できちゃうんです！！！

今回使うアプリは、、、

だん！

はい！みなさんおなじみ、、「スクリプトエディタ」さんですね！

この「スクリプトエディタ」さんで今回は、、Finderを再起動するアプリケーションを作成していきます！

## <span id="i-2">実際に作成していく</span>

作成の手順はいたって簡単です。
  
順を追って説明していきます。

  1. スクリプトエディタを起動します。
  2. 新規書類を選択します。
  3. 「do shell script &#8220;killall Finder&#8221;」と入力します。
  4. 名前(僕は「kf」としました)を設定し、ファイルフォーマットをアプリケーションにして保存します。

以上です。
  
たったこれだけです。

## <span id="i-3">起動</span>

起動方法はいろいろありますが、一番簡単なのは、Alfredですかね〜

僕は、Alfredでいつもアプリを起動するので、Alfredを起動して、速攻「kf→enter」でFinderの再起動ができます！

## <span id="i-4">おまけ</span>

実はFinderの再起動には他にも方法があります〜
  
&#8211; アクセシビリティモニターから強制終了する方法
  
&#8211; Dockアイコンのポップアップメニューから再度開くをする方法

上記の2つですかね〜
  
ただ、どっちもめんどいので、スクリプトを書いた方が楽だと思います〜

## <span id="i-5">まとめ</span>

いかがだったでしょうか、？

一瞬でしたよね、？
  
簡単でしたよね、？

スクリプトエディタは他にもいろいろと使いみちがあるので、ちょっといろいろいじってみると、、楽しいと思います〜〜
  
僕は、例えば、、ディスクキャッシュのクリーンのための「purge」もスクリプトエディタでアプリにしています！

コード
  
↓↓↓

    do shell script "sudo purge" password "***自分のパスワード***" with administrator privileges
    

よかったら試してみてください！

以上、ひろたつでした。

## <span id="i-6">参考</span>

<a href="http://inforati.jp/apple/mac-tips-techniques/system-hints/how-to-restart-the-macos-finder.html" rel="noopener" target="_blank">http://inforati.jp/apple/mac-tips-techniques/system-hints/how-to-restart-the-macos-finder.html</a>

<div style="font-size: 0px; height: 0px; line-height: 0px; margin: 0; padding: 0; clear: both;">
</div>
