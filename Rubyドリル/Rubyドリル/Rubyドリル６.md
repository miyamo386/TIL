# Rubyドリル６
### 自己解答
```ruby
def get_weather_forecast(weather)
  puts "明日の天気は#{weather}です"
end

weather = "晴れ"
get_weather_forecast(weather)

### 正解
```ruby
def get_weather_forecast(weather)
  puts "明日の天気は#{weather}です"
end

get_weather_forecast("晴れ")
```

### 学んだこと
- 引数を使用する時には、引数（実引数）に値を記述する方法もある。
- コードを記述する方法に正解はないが、シンプルなコードにすることで第三者が読んだ際に理解しやすい。
