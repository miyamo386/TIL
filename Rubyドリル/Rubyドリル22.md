# Rubyドリル22（偶数値の取得）
### 自己解答
```ruby
def count_evens(integer)
  puts integer.even?.length
end

count_evens([2, 1, 2, 3, 4])
```

### 模範解答
```ruby
def count_evens(nums)
  count = 0
  nums.each do |num|
    if num.even?
      count += 1
    end     
  end
  puts count
end
```

### 学んだこと
- 偶数の値を入れる変数を用意する必要がある。
- eachとは、配列に入っている値の数だけ処理を繰り返すメソッドのこと。
- even?とは、対象の数字が偶数かどうかを判断してture及びfalseで返すメソッドのこと。
- if文は、条件式がtureかfalseで実行する処理を分ける構文のこと。
