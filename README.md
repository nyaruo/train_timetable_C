# train_timetable_C

# 概要(Overview)
::message
```

====================================================================
  浄水駅　⇔　大曽根駅　の電車時刻表　
====================================================================

【  ソフト名  】浄水駅⇔大曽根駅の電車時刻表
【   製作者   】谷川 彩華( 学籍番号 t319058 )
【  動作環境  】コマンドプロント、power shell、windows は確認済み。
【 最終更新日 】2019/07/29
【 ファイル名 】main.c
【同梱ファイル】input.txt,read me.txt

--------------------------------------------------------------------

-概要
 浄水駅⇔大曽根駅の電車時刻表は、学校⇔私の最寄り駅の電車時間表である。
 現在時刻を読み取り、現在時刻から推測される3本分の電車の発車時刻を表示する。
 以上のこともあり、有用なアプリケーションの対象はごく一部に限られる。
 
-プログラムやデータ構造の説明
 1.利用日が平日であるか土日祝であるかをwhile文(1or2が選択されなかった際繰り返す)
　またはif文(1の時平日、2の時休日)で選択。
 2.浄水発であるか大曽根発であるかをwhile文(1or2が選択されなかった際繰り返す)
　またはif文(1のとき浄水発、2のとき大曽根発)で選択。
 3.現在時刻(時:分)をtime関数を用いて読み取り、表示する。
 4.浄水⇔大曽根の平日ダイヤ、土日祝ダイヤを構造体を格納した配列で入力している。
　※この際、timetable dayA[80]では最終電車がうまく表示されなかったため、
    timetable dayA[81]としている。他(dayB,holidayA,holidayB)も(+1)で入力している。
　そこから、電車が三本表示されるようにfor文、現在時刻から発車時刻を推測するためにif文、
　をそれぞれ用いて表示。現在時刻が終電から始発の間の場合、始発を表示するようにした。
　※この際、timetable dayA[81]において、
　　現在時刻が22:40の時22:44の次に23:08(終電)がなぜか表示されない。
　　timetabl holidayA[69], dayB[81], holidayB[73]においても同様のことが言える。 
 5.利用者の名前を入力させinput.txtに保存。
 6.プログラム終了


<参考文献>
1. Qiita, (2011).「[C言語]時間を扱う」,Kazuya Hiruma@edo_m18, https://qiita.com/edo_m18/items/364ffc6713b81c4d1c87(参照2019-7-27)
