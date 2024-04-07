# Rubyドリル３７（配列に格納された3つの数値の合計を算出するプログラム実装）
### 自己解答
```ruby
def lone_sum(ary)
end

lone_sum([1, 2, 3])
```

### 模範解答
```ruby
def lone_sum(ary)
  # 配列から、重複しない要素のみ取り出す
  uniq_nums = []
  ary.each do |num|
    count = 0
    ary.each do |i|
      if num == i
        count += 1
      end
    end
    if count < 2
      uniq_nums << num
    end
  end

  # uniq_nums配列内の合計
  sum = 0
  uniq_nums.each do |unique_num|
    sum += unique_num
  end
  puts sum
end

# 呼び出し例
lone_sum([1, 2, 3])
```

### 学んだこと
- 重複しない値を取り出す処理と、取り出した値を合計する処理に分ける必要があった。
- eachとは、配列やハッシュ内にある、要素1つずつ、繰り返し処理を行うメソッドです。
