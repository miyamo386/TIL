# Rubyドリル
### 自己解答
```ruby
class Article

  def initialize(author, title, content)
    @author = author
    @title = title
    @content = content
  end

  def 
    @author = "安倍"
    @title = "Rubyの素晴らしさについて"
    @content = "Awesome Ruby!"
  end
  
  puts "著者：#{author}"
  puts "タイトル：#{title}"
  puts "本文：#{content}"

end
```

### 正解
```ruby
class Article

  def initialize(author, title, content)
    @author = author
    @title = title
    @content = content
  end

  def author
    @author
  end

  def title
    @title
  end

  def content
    @content
  end

end

article = Article.new("阿部", "Rubyの素晴らしさについて", "Awesome Ruby!")
puts "著者: #{article.author}"
puts "タイトル: #{article.title}"
puts "本文: #{article.content}"
```

### 学んだこと
- classで定義したコードを「def メソッド名 @インスタンス名　end」と記述して専用のメソッドを用意する。
