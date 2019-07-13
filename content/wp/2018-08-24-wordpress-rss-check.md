---
title: WordPressでRSS確認方法
author: ひろたつ
type: post
date: 2018-08-23T15:10:29+00:00
url: /wordpress-rss-check/
thumbnail: 'https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/526e93904c3ede8d7d648ce64026c8ed-1.png?fit=304%2C171&ssl=1'
views:
  - 499
bzb_meta_keywords:
  - RSS確認
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
  - rss
  - wordpress

---
はいどーもー
  
ブロガーのひろたつです。

今回は、WordPressのブログを管理している人に対して、RSSの確認方法を見ていこうと思います。
  
宜しくお願い致します。

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
      <a href="#RSS"><span class="toc_number toc_depth_1">2</span> RSSとは</a>
    </li>
    <li>
      <a href="#URLRSS"><span class="toc_number toc_depth_1">3</span> URLでRSSの確認</a><ul>
        <li>
          <a href="#WordPressRSS"><span class="toc_number toc_depth_2">3.1</span> WordPressにおけるRSSの確認方法</a>
        </li>
      </ul>
    </li>
    
    <li>
      <a href="#SlackRSS"><span class="toc_number toc_depth_1">4</span> SlackでRSS連携</a>
    </li>
    <li>
      <a href="#i-2"><span class="toc_number toc_depth_1">5</span> 終わりに</a>
    </li>
  </ul>
</div>

## <span id="i">はじめに</span>

どうもです。
  
このブログの管理人をしているひろたつ</a>(<a href="https://twitter.com/hirotatsuuu" rel="noopener" target="_blank">@hirotatsuuu</a>)です。

このブログはWordPressというCMSを用いて運用しています。
  
また、テーマはXeoryを使っています（見たらわかりますがｗ

なぜ自身のサイトのRSSを知りたいのかというと、
  
僕に関しては、自分のSlackのチャンネルに自身のブログの更新を通知したいと思い、自分のRSSを確認したいなという流れです。

ですので、自分のRSSを確認した後は、SlackでRSSアプリケーション連携のやり方を書いていきます。

## <span id="RSS">RSSとは</span>

とりあえず簡単に。
  
RSSとは、「**Really Simple Syndication**」の略です。
  
Webサイトなどの更新情報や新着情報を配信するための技術のことです。

この技術を使うことで、Webサイトなどの更新、新着情報を自動的にかつ効率的にチェックすることができるのです。

## <span id="URLRSS">URLでRSSの確認</span>

まず、答えからです（笑）

WordPressではおそらく、以下のURLでRSSの確認はおｋだと思います（2018年8月現在）

    https://example.com/feed/
    

上記のexample.comという部分を自分のサイトのドメインに変えるだけでおしまいです。

が、

一応、RSSの確認方法を載せておきます。

### <span id="WordPressRSS">WordPressにおけるRSSの確認方法</span>

WordPressには、元々RSSの設定がされています。

確認のための操作はとても簡単です。

  1. サイトの管理画面に遷移
  2. 外観→ウィジェットから、メタデータをサイドバーに入れる
  3. メタデータから、自分のサイトのRSSを確認する

以上です。

ホント簡単でしたよね（笑）

## <span id="SlackRSS">SlackでRSS連携</span>

SlackでRSS連携をする方法もとても簡単です。

まず、自分のプロジェクトを作成しておきます。
  
（元々ある自分以外のプロジェクトでも良いですが、その場合は他のメンバーにバレます。それでもよければ、、、

次に、自分のアカウントをクリックした後、「その他管理項目」→「App管理」を選択します。

<div id="attachment_369" style="width: 3370px" class="wp-caption aligncenter">
  <img src="https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/fbade70bce9bb5a34068046b176cc93d.png?resize=3360%2C2100&#038;ssl=1" alt="" width="3360" height="2100" class="size-full wp-image-369" srcset="https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/fbade70bce9bb5a34068046b176cc93d.png?w=3360&ssl=1 3360w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/fbade70bce9bb5a34068046b176cc93d.png?resize=300%2C188&ssl=1 300w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/fbade70bce9bb5a34068046b176cc93d.png?resize=768%2C480&ssl=1 768w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/fbade70bce9bb5a34068046b176cc93d.png?resize=1024%2C640&ssl=1 1024w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/fbade70bce9bb5a34068046b176cc93d.png?resize=304%2C190&ssl=1 304w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/fbade70bce9bb5a34068046b176cc93d.png?resize=282%2C176&ssl=1 282w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/fbade70bce9bb5a34068046b176cc93d.png?w=2000&ssl=1 2000w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/fbade70bce9bb5a34068046b176cc93d.png?w=3000&ssl=1 3000w" sizes="(max-width: 1000px) 100vw, 1000px" data-recalc-dims="1" />
  
  <p class="wp-caption-text">
    slackのapp管理
  </p>
</div>

このような画面に遷移したでしょうか。
  
遷移していない場合は左上のslackアイコンをクリックすると遷移できると思います。

次に、検索フォームで「RSS」と検索すると、、、

RSSアプリケーションがヒットします。

そこで、自身のRSSをフィードURLという部分に入力し、投稿するチャネルを選択するだけです。

<div id="attachment_370" style="width: 3370px" class="wp-caption aligncenter">
  <img src="https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/d2def749af68dfdaf86a44eb65bbf49d.png?resize=3360%2C2100&#038;ssl=1" alt="" width="3360" height="2100" class="size-full wp-image-370" srcset="https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/d2def749af68dfdaf86a44eb65bbf49d.png?w=3360&ssl=1 3360w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/d2def749af68dfdaf86a44eb65bbf49d.png?resize=300%2C188&ssl=1 300w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/d2def749af68dfdaf86a44eb65bbf49d.png?resize=768%2C480&ssl=1 768w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/d2def749af68dfdaf86a44eb65bbf49d.png?resize=1024%2C640&ssl=1 1024w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/d2def749af68dfdaf86a44eb65bbf49d.png?resize=304%2C190&ssl=1 304w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/d2def749af68dfdaf86a44eb65bbf49d.png?resize=282%2C176&ssl=1 282w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/d2def749af68dfdaf86a44eb65bbf49d.png?w=2000&ssl=1 2000w, https://i1.wp.com/hirotatsu.me/wp-content/uploads/2018/08/d2def749af68dfdaf86a44eb65bbf49d.png?w=3000&ssl=1 3000w" sizes="(max-width: 1000px) 100vw, 1000px" data-recalc-dims="1" />
  
  <p class="wp-caption-text">
    slackでRSS
  </p>
</div>

以上です。とても簡単でしたよね？

## <span id="i-2">終わりに</span>

以上が、WordPressにおけるRSSの確認方法です。

<a href="http://berss.com/feed/Find.aspx" rel="noopener" target="_blank">http://berss.com/feed/Find.aspx</a>
  
↑↑↑
  
このようなサイトで確認ができるという記事がいくつかありましたが、できませんでした。涙

なので、自分で確認しましょう！笑

以上、ひろたつ</a>(<a href="https://twitter.com/hirotatsuuu" rel="noopener" target="_blank">@hirotatsuuu</a>)でした。

ちなみに、現在ニュージーランドで<a href="https://hirotatsu.me/wwoof-nz/" rel="noopener" target="_blank">WWOOF</a>というサービスを使って滞在しています。
  
毎日、ニュージーランド滞在記を書いていますので、見ていただけると嬉しいです。

こんな感じ
  
↓↓↓

<blockquote class="wp-embedded-content" data-secret="a6Aap0UduU">
  <p>
    <a href="https://hirotatsu.me/mt-hobson/">グレートバリア島で最も高い山マットホブソンってどんな山？</a>
  </p>
</blockquote>

<iframe class="wp-embedded-content" sandbox="allow-scripts" security="restricted" style="position: absolute; clip: rect(1px, 1px, 1px, 1px);" src="https://hirotatsu.me/mt-hobson/embed/#?secret=a6Aap0UduU" data-secret="a6Aap0UduU" width="500" height="282" title="&#8220;グレートバリア島で最も高い山マットホブソンってどんな山？&#8221; &#8212; 世界のひろたつから" frameborder="0" marginwidth="0" marginheight="0" scrolling="no"></iframe>

<div style="font-size: 0px; height: 0px; line-height: 0px; margin: 0; padding: 0; clear: both;">
</div>
