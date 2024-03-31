# Rubyドリル３１（2つの文字列の末尾の文字を比較して、一致する場合はTrue、一致しない場合はFalseを出力するプログラム）
### 自己解答
```ruby
def end_other(a, b)
  if a.downcase.slice(-1..-1) == b.downcase.slice(-1..-1)
    puts "True"
  else
    puts "False"
  end
end

end_other('Hiabc', 'abc')
```

### 模範解答
```ruby
def end_other(a, b)
  a_down = a.downcase
  b_down = b.downcase
  a_len = a_down.length
  b_len = b_down.length
  if b_down.slice(-(a_len)..- 1) == a_down || a_down.slice(-(b_len)..- 1) == b_down
    puts "True"
  else
    puts "False"
  end
end

end_other('Hiabc', 'abc')
```

### 学んだこと
- downcaseとは、大文字を小文字に変換するメソッドです。
- downcaseメソッドで小文字に変換した文字列を変数に入れる必要がある。
- sliceの範囲指定とは、切り取る範囲を指定し、slice(-3..-1)と記述した場合、「後ろ３番目から後ろ１番目を切り取る」となります。
