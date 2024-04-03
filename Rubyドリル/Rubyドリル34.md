# Rubyドリル
### 自己解答
```ruby
def array_count9(nums)
  puts nums.count(9)
end

array_count9([1, 2, 9])
```

### 模範解答
```ruby
def array_count9(nums)
  count = nums.count(9)
  puts ("配列の中には9が#{count}個です")
end

array_count9([1, 2, 9])
```

### 学んだこと
- countとは、配列や文字列などのオブジェクトが持つ要素の数をカウントするメソッドです。
- 引数がない場合は、全要素の数をカウントします。
