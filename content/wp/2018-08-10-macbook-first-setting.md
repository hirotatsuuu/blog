---
title: 僕がMacbookを買ってから最初にしたこと
author: ひろたつ
type: post
date: 2018-08-10T02:18:42+00:00
url: /macbook-first-setting/
views:
  - 144
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
  - macbook

---
はいどーもー
  
元エンジニアのひろたつです。

先日、新しいMacbookProを購入しました〜！！！
  
なので、そのNew PCに最低限の開発環境を構築するまでをやろうと思います〜！

<!--more-->

<div id="toc_container" class="toc_transparent no_bullets">
  <p class="toc_title">
    本記事の内容
  </p>
  
  <ul class="toc_list">
    <li>
      <a href="#i"><span class="toc_number toc_depth_1">1</span> インストールするアプリ</a><ul>
        <li>
          <a href="#XCode"><span class="toc_number toc_depth_2">1.1</span> XCodeインストール</a>
        </li>
        <li>
          <a href="#homebrew"><span class="toc_number toc_depth_2">1.2</span> homebrewインストール</a>
        </li>
        <li>
          <a href="#fish"><span class="toc_number toc_depth_2">1.3</span> fishインストール</a>
        </li>
        <li>
          <a href="#i-2"><span class="toc_number toc_depth_2">1.4</span> ログインシェルの変更</a>
        </li>
      </ul>
    </li>
    
    <li>
      <a href="#fish-2"><span class="toc_number toc_depth_1">2</span> fishの設定</a><ul>
        <li>
          <a href="#fisherman"><span class="toc_number toc_depth_2">2.1</span> fisherman</a>
        </li>
        <li>
          <a href="#fzf"><span class="toc_number toc_depth_2">2.2</span> fzf</a>
        </li>
        <li>
          <a href="#peco"><span class="toc_number toc_depth_2">2.3</span> peco</a>
        </li>
        <li>
          <a href="#cd-ll"><span class="toc_number toc_depth_2">2.4</span> cd > ll設定</a>
        </li>
      </ul>
    </li>
    
    <li>
      <a href="#i-3"><span class="toc_number toc_depth_1">3</span> まとめ</a>
    </li>
  </ul>
</div>

## <span id="i">インストールするアプリ</span>

僕が最低限インストールするアプリケーションはこれらです！！

  1. iTerm
  
    <a href="https://www.iterm2.com/" rel="noopener" target="_blank">https://www.iterm2.com/</a>

やっぱり、Macといったらitermですよね〜
  
標準で入っているターミナルは、、ちょっと使いづらいです。。。

  1. VSCode
  
    <a href="https://code.visualstudio.com/" rel="noopener" target="_blank">https://code.visualstudio.com/</a>

今は、、VSCode一択でしょう！（笑）
  
このエディタさえあれば、、、一応どんな言語でも対応していますね〜

  1. XCode
  
    <a href="https://developer.apple.com/jp/xcode/" rel="noopener" target="_blank">https://developer.apple.com/jp/xcode/</a>

MacのIDEですね〜
  
Appleのアプリを開発するときは必須です！
  
そして、他にも、なんか依存があるらしく、、、とりあえずインストールしときますｗ

### <span id="XCode">XCodeインストール</span>

    xcode-select --install
    

これだけです！

### <span id="homebrew">homebrewインストール</span>

<a href="https://brew.sh/index_ja" rel="noopener" target="_blank">https://brew.sh/index_ja</a>

Mac用のパッケージマネージャーと言ったらこれですよね！
  
コマンド一発でインストール可能！

### <span id="fish">fishインストール</span>

ターミナルを開いて、、、

    brew install fish
    

上のコマンド一発でfishというシェルがインストールされます!

fishとは、、フレンドリーなシェル。ｗ
  
<a href="https://fishshell.com/" rel="noopener" target="_blank">https://fishshell.com/</a>

インストールするだけで、我々が求めている機能は一通り入っている！
  
だから、zshの設定ファイルが肥大化するようなことはありません〜！

    fish -v
    

一応確認！

### <span id="i-2">ログインシェルの変更</span>

    sudo vi /etc/shells
    

編集します！

    /usr/local/bin/fish
    

最後の行に上の一行を追加します！

    chsh -s /usr/local/bin/fish
    

変更します！

以上！ｗ

## <span id="fish-2">fishの設定</span>

    touch $HOME/.config/fish/config.fish
    

上のパスにconfig.fishというファイルを作成します。
  
これが、fishシェルの設定ファイルです！

aliasとかもろもろ自分色に染めましょう〜（笑）

### <span id="fisherman">fisherman</span>

fishのプラグインマネージャーといったらfishermanですね〜
  
一昔前は、oh-my-fishというものがあったらしいです。
  
(僕は知りません、時代ですね〜ｗｗｗ

    curl -Lo ~/.config/fish/functions/fisher.fish --create-dirs https://git.io/fisher
    

上のコマンド一発で入ります！

    fisher -v
    

一応確認！

### <span id="fzf">fzf</span>

    fisher fzf
    

    brew install fzf
    

config.fishに以下を追加

    function fish_user_key_bindings
        # fzf
        bind \ce __fzf_find_file
    end
    

これで、ctrl+eでfzfが使います！

### <span id="peco">peco</span>

    fisher peco
    

    brew install peco
    

config.fishに以下を追加

    function fish_user_key_bindings
        # peco
        bind \cr peco_select_history
    end
    

上から順番に実行した場合、fzfのキーバインドがあると思うので、その場合は追記で！

これで、ctrl+rでpecoが使えます！

### <span id="cd-ll">cd > ll設定</span>

config.fishに以下を追加

    function cd
      builtin cd $argv
      ll
    end
    

これで、、cdコマンドでディレクトリを移動したときに、移動後に自動的にllコマンドを実行してくれます！
  
べんりだよ〜〜

## <span id="i-3">まとめ</span>

まだまだ、足りない設定がいくつもありますが、、一旦はこれで、ｗ

以上、ターミナルエミュレータとエディタさえあれば、開発はできるでしょう！（笑）
  
(本当はもっとほしいですが、、、Sequel ProとかDBクライアントも入れたほうがいいですよね、、ｗ

以上、ひろたつでした。

<div style="font-size: 0px; height: 0px; line-height: 0px; margin: 0; padding: 0; clear: both;">
</div>
