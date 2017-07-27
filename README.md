#### 参考
http://ruby-rails.hatenadiary.com/entry/20150415/1429031791

#### Draper
Draperはデコレーター(ビューとモデルの中間の処理を引き受ける)で、railsのプレゼンテーション層を担う。
表示に関するロジックをプレゼンテーション層に引き渡すことで、以下のようなことが避けられる。
- モデルに表示ロジックを記述
- ビューファイル内のif文多用
- helperの名前空間の衝突
結果、コードの可読性、保守性を向上することができる。

#### draperをインストール
```ruby
gem 'draper', '~> 1.3'
```
`$ bundle install`

#### 土台となるアプリケーションを作成
`$ rails g scaffold Blog title:string content:text
