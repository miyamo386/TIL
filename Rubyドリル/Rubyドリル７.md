# Rubyドリル７
### 自己解答
```ruby
require "date"

def Display_week()
  if 
    puts "今日は#{}だ！！"
  else
    puts "今日は#{}"
  end
  
end

week = Date.today.wday

Display_week()
```

### 正解
```ruby
require "date"

day = Date.today.wday
days = ["日曜日", "月曜日", "火曜日", "水曜日", "木曜日", "金曜日", "土曜日"]

if day == 5
  puts "今日は#{days[day]}だ！！！"
else
  puts "今日は#{days[day]}"
end
```

### 学んだこと
- Dateクラスとは、曜日・日付などを管理するRubyの標準ライブラリです。
- wdayとは、Dateクラスのメソッドで、曜日を0(日曜日)から6(土曜日)の数字で取得します。
