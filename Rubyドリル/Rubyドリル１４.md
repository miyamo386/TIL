# Rubyドリル１４（if,else問題）
### 自己解答
```ruby
def in1to10(num, outside_mode)
  if  || num >= 1 && num <= 10

　　　　else

  end
end

in1to10(5,false)
in1to10(11,false)
in1to10(11,true)
```

### 模範解答
```ruby
def in1to10(num, outside_mode)
  if (num >= 1 && num <= 10) || outside_mode
    puts "True"
  else
    puts "False"
  end
end

in1to10(5,false)
in1to10(11,false)
in1to10(11,true)
```

### 学んだこと
- 論理演算子とは、条件式のTrueやFalseを確認できる、記号や符号のことです。
- Rubyの論理演算子、左から右に条件式を判別し、確定した時点で終了となります。
