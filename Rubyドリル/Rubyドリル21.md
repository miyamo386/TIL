# Rubyドリル21（指定した範囲の数値によって処理が異なるプログラム）
### 自己解答
```ruby
def parrot_trouble(talking, hour)
  if talking && false || hour 
    puts "OK"
  else
    puts "NG"
  end

end

parrot_trouble(true, 6)
parrot_trouble(true, 7)
parrot_trouble(false, 6)
parrot_trouble(false, 7)
```

### 模範解答
```ruby
def parrot_trouble(talking, hour)
  if talking && (hour < 7 || hour > 20)
    puts "NG"
  else
    puts "OK"
  end
end

# 呼び出し例
parrot_trouble(true, 6)
```

### 学んだこと
- talking && (hour < 7 || hour > 20)を言語化すると、talkingがtrueで、hourは７以下または、２０以下の場合となります。
