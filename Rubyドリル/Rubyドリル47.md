# Rubyドリル
### 自己解答
```ruby
movie = {"title" => "ハリーポッター", "genre" => "ファンタジー", "year" => "2001年"}
gets "以下から一つを選んで入力してください。"
puts movie[title]
```

### 模範解答
```ruby
def movie_info(movie, data)
  puts movie[data]
end

movie = {title: "ハリーポッター", genre: "ファンタジー",  year: "2001年"}

puts "以下から一つを選んで入力してください。
  ・title
  ・genre
  ・year"

info = gets.chomp.to_sym

movie_info(movie, info)
```

### 学んだこと
- chompとは、文字列の後ろにある改行を取り除くメソッドです。
- ハッシュとは、データと名前のセットで管理すつデータの構造です。
- to_symとは、文字列をシンボルに変えるメソッドで、今回は文字列をシンボルに変換して、ハッシュのキーとして使用しました。
