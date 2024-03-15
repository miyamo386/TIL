# Rubyドリル
### 自己解答
```ruby
def output(input)
  input.times do
    puts "Hello!"
  end
end

puts "何回表示させますか？"
input = gets.to_i

output(input)
```

### 模範解答
```ruby
def output(num)
  num.times do
    puts "Hello!" 
  end
end

puts "何回表示させますか？"
num = gets.to_i
output(num)
```

### 学んだこと
- getsメソッドの出力は文字列となるため、to_iメソッドで数字に変換します。
- timesとは、指定した数字（値）の数だけ繰り返し処理を行うメソッドです。
- 変数（input）の値には、数字が入っている。
