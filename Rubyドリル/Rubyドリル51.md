# Rubyドリル
### 自己解答
```ruby
def register_book
  # 本の著者、タイトル、価格をユーザーに入力させ、保存する
  puts '著者を入力してください'
  puts 'タイトルを入力してください'
  puts '価格を入力してください'

  book = { author: author, title: title, price: price }

end

def show_books(books)
  puts "見たい番号を入力してください"
  # 保存された本の一覧を出力する
end

def show_detail
  # 選択された本の詳細な情報（著者、タイトル、価格）を出力する
  puts "著者 #{book[:author]}"
  puts "タイトル #{book[:title]}"
  puts "価格 #{book[:price]}円"
end


while true do
  puts "番号を入力してください"
  puts "0: 本を登録する"
  puts "1: 本の一覧を見る"
  puts "2: 終了する"
  case gets.to_i
  when 0
    # 本の登録を行う
  when 1
    # 保存された本の一覧を出力する
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
  puts "見たい番号を入力してください"
  index = 1
  books.each do |book|
    puts "#{index}: #{book[:title]}"
    index += 1
  end
  input = gets.to_i
  show_detail(books[input - 1])
end
```

### 学んだこと
- <<とは、ハッシュを配列に追加する演算子です。
