# Rubyドリル
### 自己解答
```ruby
def post_item(a_cart)
  puts "商品名を入力してください："
  name = gets.chomp
  puts "値段を入力してください："
  price = gets.to_i
  puts "個数を入力してください："
  quantity = gets.to_i
  line = {name: name, price: price, quantity: quantity}

  puts "商品名 : #{line.name}"
  puts "値段 : #{line.price}"
  puts "個数 : #{line.quantity}"
  puts "合計金額 : #{line.price * line.quantity}"

  lines >> line
# a_cartをメソッドの呼び出し元に返す

end

def check_items(a_cart)
# 保存された全ての商品情報（商品名・値段・個数）を、商品ごとに表示する

# 全ての商品の合計金額を表示する
  puts "合計金額 : "

end

def end_program
  # プログラムを終了させる
end

def exception
  puts "入力された値は無効な値です"
end

cart = []             # 配列オブジェクトcartの生成

while true do
# メニューの表示
  puts "商品数: #{cart.length}"
  puts "[0]商品をカートに入れる"
  unless cart.empty?       #カートに商品がない場合、[1]は選択不可
    puts "[1]カートを確認する"
  end
  puts "[2]アプリを終了する"
  input = gets.to_i

  if input == 0 then
    cart = post_item(cart)  # post_itemメソッドを呼び出す記述
  elsif input == 1 then
    check_items(cart) # check_itemsメソッドを呼び出す記述
  elsif input == 2 then
    end_program     # end_programメソッドを呼び出す記述
  else
    exception           # exceptionメソッドを呼び出す記述
  end
end
```

### 模範解答
```ruby
def post_item(a_cart)
  # 変数の定義
  post = {}
  puts "商品名を入力してください："
  post[:name] = gets.chomp
  puts "値段を入力してください："
  post[:price] = gets.to_i
  puts "個数を入力してください："
  post[:count] = gets.to_i
  line = "---------------------------"

  # レビューの描画
  puts "商品名 : #{post[:name]}\n#{line}"
  puts "値段 : #{post[:price]}\n#{line}"
  puts "個数 : #{post[:count]}\n#{line}"
  puts "合計金額 :#{post[:price] * post[:count]}\n#{line}"

  # 配列オブジェクトに追加
  a_cart << post

  # a_cartをメソッドの呼び出し元に返す
  return a_cart
end

def check_items(a_cart)
  # リストの表示
  total_price = 0
  line = "---------------------------"
  a_cart.each do |post|
    puts "#{post[:name]}/#{post[:price]}/#{post[:count]}\n#{line}"
    total_price += post[:price] * post[:count]
  end
  puts "合計金額 : #{total_price}"
end

def end_program
  exit
end

def exception
  puts "入力された値は無効な値です"
end

cart = []         # 配列オブジェクトcartの生成

while true do
  # メニューの表示
  puts "商品数: #{cart.length}"
  puts "[0]商品をカートに入れる"
  unless cart.empty?
    puts "[1]カートを確認する"
  end
  puts "[2]アプリを終了する"

  input = gets.to_i

  if input == 0 then
    cart = post_item(cart)  # post_itemメソッドの呼び出し
  elsif input == 1 then
    check_items(cart) # check_itemsメソッドの呼び出し
  elsif input == 2 then
    end_program    # end_programメソッドの呼び出し
  else
    exception        # exceptionメソッドの呼び出し
  end
end
```

### 学んだこと
- \n#{line}とは、\nで改行した箇所に、lineを挿入することで、今回は"---------------------------"が挿入されます。
