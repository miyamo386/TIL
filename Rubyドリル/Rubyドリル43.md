# Rubyドリル
### 自己解答
```ruby
class Book
  attr_reader :title
  attr_reader :price

  def initialize(title, price)
    @title = title
    @price = price
  end
end

book = Book.new("毒を持て", 100)
puts book.title
puts book.price
```

### 模範解答
```ruby
class Book
  attr_reader :title, :price

  def initialize(title, price)
   @title = title
   @price = price
  end
end

book = Book.new("プロを目指す人のためのRuby入門", 3218)
puts book.title
puts "#{book.price}円"
```

### 学んだこと
- 
