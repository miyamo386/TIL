# Rubyドリル３６（銀行口座に10万円の預金残高があり、お金を引き出すプログラム実装）
### 自己解答
```ruby
def withdraw(balance, amount)
  fee = 110
  if 

    puts "#{amount}円引き落としました。残高は#{count}円です"
  else
    puts "残高不足です"
  end
end

balance = 100000
puts "いくら引き落としますか？（手数料110円かかります）"
money = gets.to_i
withdraw(balance, money)
```

### 模範解答
```ruby
def withdraw(balance, amount)
  fee = 110
  if balance >= (amount + fee)
    balance -= (amount + fee)
    puts "#{amount}円引き落としました。残高は#{balance}円です"
  else
    puts "残高不足です"
  end
end

balance = 100000
puts "いくら引き落としますか？（手数料110円かかります）"
money = gets.to_i
withdraw(balance, money)
```

### 学んだこと
- 条件式を、預金残高（balance）が引き落とし額（money）と手数料（fee）の合計より多いかで判別しています。
- -=とは、変数に代入された値を指定した数値だけ減算する演算子です。
