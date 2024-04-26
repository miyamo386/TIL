# Rubyドリル
### 自己解答
```ruby
def register_data
  # データの登録という文字列を表示させる
end

def show_data
  # データの確認という文字列を表示させる
end

while true
  puts "選択してください"
  puts "[0]登録する"
  puts "[1]データを確認する"
  puts "[2]終了する"
  input = gets.to_i

  if input == 0
    # データの登録と出力するための関数を呼ぶ
  elsif input == 1
    # データの確認と出力するための関数を呼ぶ
  elsif input == 2
    # アプリケーションを終了させる
  else

  end
end
```

### 模範解答
```ruby
def register_data
  puts "データの登録"
end

def show_data
  puts "データの確認"
end

while true
  puts "選択してください"
  puts "[0]登録する"
  puts "[1]データを確認する"
  puts "[2]終了する"
  input = gets.to_i

  if input == 0
    register_data
  elsif input == 1
    show_data
  elsif input == 2
    exit
  else
    puts "無効な値です"
  end
end
```

### 学んだこと
- whileとは、指定した条件がtureの間、処理を繰り返すRubyの構文です。
- while文の「do」は省略することができる。
