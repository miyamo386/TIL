# Rubyドリル11（特定の文字列を検知するプログラムの実装）
### 自己解答
```ruby
def check_name(str) 
  if 

  else
    puts str.include?(.)

   puts str.include?( )
end

puts "登録したい名前を入力してください(例)YamadaTaro"
str = gets
check_name(str)
```

### 模範解答
```ruby
def check_name(str) 
  if str.include?(".")
    puts "!エラー!記号は登録できません"
  elsif str.include?(" ")
    puts "!エラー!空白は登録できません"
  else
    puts "登録が完了しました"
  end
end
puts "登録したい名前を入力してください(例)YamadaTaro"
str = gets
check_name(str)
```

### 学んだこと
- include?とは、指定した値が、配列の中に含まれているのかを判別するメソッドです。
- elsifとは、２つ目以降に条件式を追加するif構文です。
- getsとは、文字入力機能を起動するメソッドです。
