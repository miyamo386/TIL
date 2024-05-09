# Rubyドリル
### 自己解答
```ruby
def registration_student
  student = {}
  puts '生徒名を入力してください'
  name = gets.chomp
  puts '生徒の年齢を入力してください'
  age = gets.to_i
  puts "国語の得点は？"
  kokugo = gets.to_i
  puts "数学の得点は？"
  maths = gets.to_i
  puts "英語の得点は？"
  english = gets.to_i

  student = {name: name, age: age, kokugo: kokugo, maths: maths, english: english}

  students  << student
end

def show_student_name
  # 登録された生徒の名前を番号を振って表示しなさい
  puts '見たい生徒の番号を入力してください'

  # 選択された生徒の名前、年齢、国語、数学、英語の点数を表示できるようにしなさい
  puts "名前:"
  puts "年齢:"
  puts "国語:"
  puts "数学:"
  puts "英語:"
end

students = []

while true
  puts '行いたい項目を選択してください'
  puts '[1]点数を登録する'
  puts '[2]点数を確認する'
  puts '[3]終了する'
  input = gets.to_i
  if input == 1
    registration_student
  elsif input == 2
    show_student_name
  elsif input == 3
    exit
  else
    puts '無効な値です'
  end
end
```

### 模範解答
```ruby
def registration_student(students)
  # 生徒の名前と年齢を登録できるようにしなさい
  student = {}
  puts '生徒名を入力してください'
  student[:name] = gets.chomp
  puts '生徒の年齢を入力してください'
  student[:age] = gets.chomp

  # 登録した生徒の国語、数学、英語の点数を登録できるようにしなさい
  puts "国語の得点は？"
  student[:japanese] = gets.to_i
  puts "数学の得点は？"
  student[:math] = gets.to_i
  puts "英語の得点は？"
  student[:english] = gets.to_i
  students << student

end

def show_student_name(students)
  # 登録された生徒の名前を番号を振って表示しなさい
  i = 0
  students.each do |student|
    puts "#{i}: #{student[:name]}"
    i += 1
  end
  puts '見たい生徒の番号を入力してください'
  num = gets.to_i

  student = students[num]
  # 選択された生徒の名前、年齢、国語、数学、英語の点数を表示できるようにしなさい
  puts "名前: #{student[:name]}"
  puts "年齢: #{student[:age]}"
  puts "国語: #{student[:japanese]}"
  puts "数学: #{student[:math]}"
  puts "英語: #{student[:english]}"
end

students = []

while true
  puts '行いたい項目を選択してください'
  puts '[1]点数を登録する'
  puts '[2]点数を確認する'
  puts '[3]終了する'
  input = gets.to_i
  puts input
  if input == 1
    registration_student(students)
  elsif input == 2
    show_student_name(students)
  elsif input == 3
    exit
  else
    puts '無効な値です'
  end
end
```

### 学んだこと
- ハッシュを定義し、変数名[:キー名]に代入することで値をハッシュに保存できる。
