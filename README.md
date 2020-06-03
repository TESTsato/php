github markdown 記法
このサイトは [GitHubのMarkdownについて](https://help.github.com/ja/github/writing-on-github/basic-writing-and-formatting-syntax)

以下がマニュアル
https://httpd.apache.org/docs/2.4/programs/apachectl.html

apache のコマンドリスト
```
sudo apachectl start
sudo apachectl stop
```

# web ページ情報取得例
```
<?php

// file_get_contents
$url = "https://github.com/SenKaonashi/learn/edit/master/README.md";
$html = file_get_contents($url);
// echo $html;
// var_dump($html);

// curl
$ch = curl_init(); 
curl_setopt($ch, CURLOPT_URL, $url); 
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
$info = curl_getinfo($ch);
curl_close($ch);

//var_dump($info);
?>
```
