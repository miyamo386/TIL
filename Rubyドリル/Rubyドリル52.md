# Rubyドリル５２
### 自己解答
```ruby
def register_book(books)
  puts '著者を入力してください'
  author = gets.chomp
  puts 'タイトルを入力してください'
  title = gets.chomp
  puts '価格を入力してください'
  price = gets.to_i
  book = { author: author, title: title, price: price }
  books << book
end

def show_books(books)
  puts "見たい番号を入力してください"
  index = 1
  books.each do |book|
    puts "#{index}: #{book[:title]}"
    index += 1
  end
  input = gets.to_i
  show_detail(books[input - 1])
end

def show_detail(book)
  puts "著者 #{book[:author]}"
  puts "タイトル #{book[:title]}"
  puts "価格 #{book[:price]}円"
end

books = []
while true do
  puts "番号を入力してください"
  puts "0: 本を登録する"
  puts "1: 本の一覧を見る"
  puts "2: 終了する"
  case gets.to_i
  when 0
   register_book(books)
  when 1
    show_books(books)
  when 2
    exit
  else
    puts '無効な値です'
  end
end
```

### 模範解答
```ruby
def register_book(books)
  puts '著者を入力してください'
  author = gets.chomp
  puts 'タイトルを入力してください'
  title = gets.chomp
  puts '価格を入力してください'
  price = gets.to_i
  book = { author: author, title: title, price: price }
  books << book
end

def show_books(books)
  puts "平均価格: #{average_price(books)}円"
  puts "見たい番号を入力してください"
  index = 1
  books.each do |book|
    puts "#{index}: #{book[:title]}"
    index += 1
  end
  input = gets.to_i
  show_detail(books[input - 1])
end

def show_detail(book)
  puts "著者 #{book[:author]}"
  puts "タイトル #{book[:title]}"
  puts "価格 #{book[:price]}円"
end

def average_price(books)
  total = 0
  books.each do |book|
    total += book[:price]
  end
  average = total / books.length
end

books = []
while true do
  puts "番号を入力してください"
  puts "0: 本を登録する"
  puts "1: 本の一覧を見る"
  puts "2: 終了する"
  case gets.to_i
  when 0
   register_book(books)
  when 1
    show_books(books)
  when 2
    exit
  else
    puts '無効な値です'
  end
end
```

### 学んだこと
- eachで、「books」にある要素を取り出した後、「price」のみを「+=」にて変数「total」に代入する。
- lengthで本の数を出力している。
