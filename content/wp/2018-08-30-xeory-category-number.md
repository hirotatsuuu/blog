---
title: 【WordPress】xeoryテーマでサイドバーのカテゴリーの数を改行しないで表示させる方法
author: ひろたつ
type: post
date: 2018-08-30T13:56:37+00:00
url: /xeory-category-number/
thumbnail: 'https://i0.wp.com/hirotatsu.me/wp-content/uploads/2018/08/b0bb4eec57ff92d9b3071fbbe7155624.png?fit=304%2C171&ssl=1'
views:
  - 115
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
  - カテゴリー数
  - サイドバー

---
はいどーもー
  
絶賛ニート中で家で記事を書いているひろたつです。

今回は、wordpressのテーマである、xeoryテーマの編集についてです！
  
サイドバーにカテゴリーの数を表示させると改行されてしまうので、その修正方法をシェアしようと思います。

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
      <a href="#i-2"><span class="toc_number toc_depth_1">2</span> サイドバーのカテゴリー数を改行しないで表示するように修正</a><ul>
        <li>
          <a href="#i-3"><span class="toc_number toc_depth_2">2.1</span> うまくいかない場合</a>
        </li>
      </ul>
    </li>
    
    <li>
      <a href="#i-4"><span class="toc_number toc_depth_1">3</span> おわりに</a>
    </li>
  </ul>
</div>

## <span id="i">はじめに</span>

この記事を見ているということは、みなさんはWordPressでブログを運営しているのだと思います。
  
そして、xeoryという無料のテーマを使っているのではないでしょうか？

<a href="https://xeory.jp/" rel="noopener" target="_blank">https://xeory.jp/</a>

こちらがxeoryテーマです。
  
バズ部が作成しているテーマでシンプルでかっこいいテーマを無料で使うことができます！
  
僕のおすすめなので、ぜひ、！笑

ただ、配布されているテーマを使っているとたまに問題が、、、

デフォルトの状態だとなんかちがうな〜
  
自分好みのテーマにしたいな〜

って思うことないですか？

xeoryテーマを使っていると、たまにこの問題にぶち当たります。

そして、、、今回の問題が、

「サイドバーにカテゴリーの数を表示するように設定すると、改行されてしまう」

というものです。

なんか、、ださいんですよねｗ

別にこのままでも良いんですけど、、、なんかねｗ

というわけで修正しちゃいましょう〜

## <span id="i-2">サイドバーのカテゴリー数を改行しないで表示するように修正</span>

はい、修正していきます〜

今回編集するファイルは、style.cssです。

style.cssファイルから「.widget_categories a」という部分を探してください。
  
（僕の場合は1197行目あたりにありました。）
  
そして、下の様になるようにdisplayを修正してください



簡単に言うと、

display: block;
  
を
  
display: inline-block;
  
に修正するだけです。

以上でおしまいです。

### <span id="i-3">うまくいかない場合</span>

うまくいかない場合は、いくつか可能性を考えてみましょう。

  1. ブラウザキャッシュにより変更が反映されていない
  
    → シークレットモードなどにして確認してみてください</p> 
  2. テーマのカラー設定を変更している
  
    → この場合は、追記するコードが多少変わります。



## <span id="i-4">おわりに</span>

いかがだったでしょうか？
  
うまく変更できましたか？

これで、スタイリッシュなブログになったと思います。

ここまで読んでくださりありがとうございました。

以上、ひろたつでした。

<div style="font-size: 0px; height: 0px; line-height: 0px; margin: 0; padding: 0; clear: both;">
</div>
