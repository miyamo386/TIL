# Rubyドリル
### 自己解答
```ruby
def sleep_in(is_weekday, is_vacation)
  if is_weekday && is_vacation || 
    puts "True"
  else
    puts "False"
  end
end

sleep_in(false, false)
sleep_in(true, false)
sleep_in(false, true)
```

### 模範解答
```ruby
def sleep_in(is_weekday, is_vacation)
  if (is_weekday != true) || (is_vacation == true)
    puts true
  else
    puts false
  end
end

# 呼び出し例
sleep_in(false, false)
```

### 学んだこと
- 演算子||は、左辺か右辺どちらかの条件式がtrueの場合に処理を実行する。
