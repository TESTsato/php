mac による artisan serve コマンド実行まで　
https://getcomposer.org/download/
https://readouble.com/laravel/7.x/ja/installation.html

以下により、composer の設定
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'e0012edf3e80b6978849f5eff0d4b4e4c79ff1609dd1e613307e16318854d24ae64f26d17af3ef0bf7cfb710ca74755a') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"

プロジェクトの作成と、ディレクトリの移動
composer create-project --prefer-dist laravel/laravel blog
cd blog/
