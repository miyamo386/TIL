# Rubyドリル
### 自己解答
```ruby
def addition(a, b)

end

def multiplication(a,b)

end

def slice_num(num)
  # 10の位の計算

  # 1の位の計算

end

puts "二桁の整数を入力してください"
input = gets.to_i

X, Y = slice_num(input)
#  additionメソッドにX,Yを引数として渡し、処理結果を変数add_resultに代入する。

#  multiplicationメソッドにX,Yを引数として渡し、処理結果を変数multiple_resultに代入する。

puts "足し算結果と掛け算結果の合計値は#{add_result + multiple_result}です"
```

### 模範解答
```ruby
def addition(a, b)
  a + b
end

def multiplication(a,b)
  a * b
end

def slice_num(num)
  # 10の位
  tens_place = (num / 10) % 10
  # 1の位
  ones_place = num % 10
  return tens_place, ones_place
end

puts "二桁の整数を入力してください"
input = gets.to_i
X, Y = slice_num(input)
add_result = addition(X, Y)
multiple_result = multiplication(X, Y)
puts "足し算結果と掛け算結果の合計値は#{add_result + multiple_result}です"
```

### 学んだこと
- 任意の桁の数字を取り出す方法は、取り出したい数字の桁で割り、さらに１０で割るとできる。
- Rubyの性質上、整数同士の計算だと返り値は整数となり、小数点以下は切り捨てられる「。
- 変数をカンマで区切るり定義すると、同時に複数の変数を定義できる。
