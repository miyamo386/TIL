# Rubyドリル12
### 自己解答
```ruby
input = gets.to_i

if input <= 10
  puts "10以下の数字です"
elsif input <= 0
  puts "0以下の数字です"
else input > 10
  puts "10より大きい数字です"
end
```

### 模範解答
```ruby
input = gets.to_i

if input <= 0
  puts "0以下の数字です"
elsif input <= 10
  puts "10以下の数字です"
else
  puts "10より大きい数字です"
end
```

### 学んだこと
- if文は上から順に条件式が実行されます。例え下の条件式が当てはまったとしてもスルーされます。
- 「-1」を考慮する必要があり、「０以下の数字」の条件式を先に記述する。
