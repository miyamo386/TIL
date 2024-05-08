# Rubyドリル
### 自己解答
```ruby
def janken
  puts "[0]:グー\n[1]:チョキ\n[2]:パー"

  player_hand = gets.to_i

  program_hand = rand(2)

  jankens = ["グー", "チョキ", "パー"]

  puts "あなたの手:#{jankens[player_hand]}, わたしの手:#{jankens[program_hand]}"

  # あいこの判定はplayer_handとprogram_handの値が等しいとき
  if player_hand == program_hand
    puts "あいこで"
    # 返り値を返す

 # じゃんけんに勝つパターンを全て並べる
  elsif
    puts "あなたの勝ちです"
   # 返り値を返す

  else
    puts "あなたの負けです"
    # 返り値を返す

  end
end

next_game = true

puts "最初はグー、じゃんけん..."

while next_game do
# jankenメソッドの返り値をnext_gameに代入
end
```

### 模範解答
```ruby
def janken
  puts "[0]:グー\n[1]:チョキ\n[2]:パー"
  player_hand = gets.to_i

  program_hand = rand(3)

  jankens = ["グー", "チョキ", "パー"]

  puts "あなたの手:#{jankens[player_hand]}, わたしの手:#{jankens[program_hand]}"

  if player_hand == program_hand
    puts "あいこで"
    return true
  elsif (player_hand == 0 && program_hand == 1) || (player_hand == 1 && program_hand == 2) || (player_hand == 2 && program_hand == 0)
    puts "あなたの勝ちです"
    return false
  else
    puts "あなたの負けです"
    return false
  end
end

next_game = true

puts "最初はグー、じゃんけん..."

while next_game do
  next_game = janken
end
```

### 学んだこと
- returnとは、呼び出し元に値を返す構文です。メソッドの処理を終了する効果もあります。
