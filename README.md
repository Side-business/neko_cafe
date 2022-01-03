# laravel 環境構築

MAMPはダウンロードされているものとする

## Githubからクローンする

MAMP/htdocs/上で以下を実行

$ git clone git@github.com:Side-business/neko_cafe.git

## PHPのバージョン確認

$ php -v

PHP 7.1.14 (cli)のような文字が出てくるので、数字が７.０以上であればOK。

もしPHPが７.０以下ならば、PHPをアップデートする必要あり。

## Homebrewのインストール

以下のコマンドをターミナルで打って、Homebrewをインストールする。

$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
 
インストールできたら次にPHPをインストールする。バージョン７.2をインストールする。

$ brew install php@7.2

## Composerのインストール

次にLaravelをインストールするためにComposerというPHPのパッケージマネージャーをインストールする。

$ brew install homebrew/core/composer

PATHを通して、composer のコマンドを使えるようする。

$ export PATH="$PATH:$HOME/.composer/vendor/bin"

## LaravelをMAMPで起動

neko_cafeのディレクトリに移動して

$ cd MAMP/htdocs/neko_cafe

ローカルサーバーを起動する（rails s 的なやつ）

$ php artisan serve

http://localhost:8888/
にアクセスする