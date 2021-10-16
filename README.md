# train_timetable_C

# 概要(Overview)

- 本アプリは、浄水駅 <-> 大曽根駅　の電車時刻表アプリです。  
(This application is a train timetable application between Josui Station and Ozone Station.)
- 現在時刻を読み取り、現在時刻から推測される3本分の電車の発車時刻を表示する。  
(It reads the current time and displays the departure time of three trains estimated from the current time.)
- 以上のこともあり、有用なアプリケーションの対象は自身の個人利用に限られる。  
(From the above, the object of the useful application is limited to one's own personal use.)

# プログラムやデータ構造の説明(Structure Description)
1.　利用日が平日か休日かを選択(Select weekday or holiday)  
  whileで繰り返し、 ifで選択  
 
 
2.　浄水駅発か大曽根駅発かを選択(Select whether to depart from Josui Station or Ozone Station)  
  while文で繰り返し、 ifで選択  
 
 
3.現在時刻を読み取り表示(Read and display the current time)  
  time関数で現在時刻を読み取り
  
  
4.現在自国から発車時刻を推定して表示(Estimate and display the departure time from the current time)  
  for文で3つの時間を表示、 if文で発車時刻を推測、また、現在時刻が終電から始発の間の場合、始発を表示するようにした  
  浄水駅 <-> 大曽根駅の平日ダイヤ、土日祝ダイヤを構造体を格納した配列を用いて入力  
  (Input weekday and holiday timetables using an array that stores the structure)  
 構造体、　配列  
 * timetable dayA[80]では最終電車がうまく表示されなかったため、timetable dayA[81]としている。他(dayB,holidayA,holidayB)も(+1)で入力している。  
 * timetable dayA[81]において、現在時刻が22:40の時22:44の次に23:08(終電)がなぜか表示されない。  
  
  
5.利用者の名前を入力させinput.txtに保存
 
6.プログラム終了


# 参考文献(References)
Qiita, (2011).「[C言語]時間を扱う」,Kazuya Hiruma@edo_m18, https://qiita.com/edo_m18/items/364ffc6713b81c4d1c87(参照2019-7-27)
