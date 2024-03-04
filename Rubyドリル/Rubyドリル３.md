# Rubyドリル３
### 自己解答
```ruby
test_scores = [80, 50, 70]

def calculate_average(scores)
  total = scores.sum
  average = total.to_f / scores.length
end

puts "3教科の平均点は: #{calculate_average(test_scores)}です。"
```

### 正解
```ruby
japanese_score = 80
english_score = 50
math_score = 70

average_score = (japanese_score + english_score + math_score) / 3

puts "3教科の平均点は、#{average_score}点です。"
```

### 学んだこと
- AIに質問したコードをそのまま記載するのではなく、習得したスキルを活用して問題を解く事が重要だと学んだ。
- （）とは、（）の中にある処理を優先にする記述方法です。
- 式展開とは、文字列の中に「式（文字列•数字•演算子•変数•メソッドの呼び出し）」を入れる、Rubyの機能です。 
