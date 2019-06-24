# test
test
#用事の有無
puts "仕事終わりに用事はありますか？"

puts"------------------"
plan1 = ["はい","いいえ"]
  index = 0
  plan1.each do |plan1|
    puts "#{index}.#{plan1}"
    index += 1
end
puts"------------------"
plan1_anser = gets.chomp.to_i

case plan1_anser
when 0
puts "用事の内容を教えてください"
  puts"------------------"
  plan2 = ["飲み会","ジム"]
  index = 0
  plan2. each do |plan2|
    puts "#{index}.#{plan2}"
    index += 1
    end
    puts"------------------"

  plan2_anser = gets.chomp.to_i

  if plan2_anser == 0
    puts "今日はワンピースにしましょう！"
  else
    puts "スポーツウェアと靴下を忘れずにね！"
  end

when 1
puts "1日お仕事頑張り頑張りましょう！"

puts "ちなみに、今日の天気は？"
#天気を表示
  puts "------------------"
  weather = ["晴れ" , "雨"]
  index = 0
  weather. each do |weather|
    puts "#{index}.#{weather}"
    index += 1
  end
  puts "------------------"

#天気を入力

  number = gets.chomp.to_i

  selected_weather = weather[number]
  puts "今日の天気は#{selected_weather}ですね？"

#晴れコーデを提示
  if number == 0
    tops = ["白長袖", "ピンク長袖" , "カーキ長袖"]
    selected_tops = tops.sample



    case selected_tops
      when "白長袖"
        skirt = ["ベージュズボン" , "グレーズボン"]
        coat = ["ネイビーカーデ", "白カーデ" , "黄色カーデ"]
        puts "晴コーデ1と出ました！「#{selected_tops}」に「#{skirt.sample}」に「#{coat.sample}」でどうでしょう"

      when "ピンク長袖"
        skirt = "グレーズボン"
        coat = ["ネイビーカーデ", "白カーデ"]
        puts "晴コーデ2と出ました！「#{selected_tops}」に「#{skirt}」に「#{coat.sample}」でどうでしょう"

      when "カーキ長袖"
        skirt = "ベージュズボン"
        coat = ["ネイビーカーデ","黄色カーデ"]
        puts "晴コーデ3と出ました！「#{selected_tops}」に「#{skirt}」に「#{coat.sample}」でどうでしょう"
      end
#雨コーデを提示
  else
    tops = ["白半袖", "黄色半袖" , "オレンジ花柄"]
    skirt = ["青スカート", "白スカート" , "ピンクスカート"]
    coat = ["ロング白カーデ", "ロングベージュカーデ", "黄色カーデ"]
      puts "雨コーデは「#{tops.sample}」に「#{skirt.sample}」に「#{coat.sample}」でどうでしょう"
end
end
