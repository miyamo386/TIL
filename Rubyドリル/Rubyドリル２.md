# Rubyドリル２
### 自己解答
```ruby
user_data.each do |user|
  puts user[:user][:profile][:name]
end
```

### 正解
```ruby
user_data.each{ |u| puts u.dig(:user, :profile, :name) }
```

### 学んだこと
- ブロック変数を利用してハッシュの値を取得するには、ブロック変数[取得したい値のキー]と記述します。
- 二重ハッシュの値を取得する際は、[取得したい値のキー]を追記します。
- digメソッドとは、引数にハッシュの中から指定したいキーを記述する事で、値を取得できるメソッドです。
