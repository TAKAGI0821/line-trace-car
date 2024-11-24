# お菓子回収ライントレースカー
## DEMO
- **お菓子を回収する際の動画**:<br>
https://github.com/user-attachments/assets/f4543615-a7e0-47b9-b964-e427240bc20a

- **お菓子をアームロボットの前で放す際の動画**:<br>
https://github.com/user-attachments/assets/be118170-a269-487c-a4c8-76094f88b747

## コース
<b>【コースの全体像】</b><br><br>
![image](https://github.com/user-attachments/assets/b8c8beda-1d6e-4216-b009-f145990218de)

## 機体
<b>【機体の表側】</b><br>
![image](https://github.com/user-attachments/assets/48ef1e28-f26a-42b3-a2a0-4918459ea631)

<br>
<br>

<b>【機体の裏側】</b><br>
![image](https://github.com/user-attachments/assets/1c583e9e-40c4-4d4d-b086-4761cecc8d05)

<br>
<br>

<b>【工夫点】</b><br>
アッカーマン機構というモノを採用することで、左タイヤと右タイヤの水平位置のずれを最小限に抑えている。
また、これにより、タイヤによる前進方向の力の妨害を防ぐことに寄与している。<br>
左側：は両輪を1つの軸でつないでいる。<br>
右側：アッカーマン機構でタイヤをつけている。<br>

![image](https://github.com/user-attachments/assets/1819edc2-696f-4b05-a084-6b1c9962bd97)

## 回路
<b>【簡易的な回路図】</b><br>
![image](https://github.com/user-attachments/assets/63ba43ec-9fbd-433d-a468-c422b2764185)

<br>
<br>

## プログラム
流れとしては「フォトセンサでラインを走行」→「赤外線センサーとフォトセンサで箱を発見」→「箱を持っていなければ箱を拾う」→「フォトセンサでラインを走行」→「フォトセンサでアームロボットを検知し、箱を持っている場合、止まる」→「箱を放す」→同様のことを繰り返す。<br><br>
フローチャート１の左側のフローがmainフローになっており、そこを起点にセンサーの読み取り、お菓子の取捨などの処理を行っている。

<br>

<b>【フローチャート1】</b><br>

![image](https://github.com/user-attachments/assets/12a25cf1-e34b-46ff-839b-11eabb86d1c3)

<br>

<b>【フローチャート2】</b><br>

![image](https://github.com/user-attachments/assets/d67c6a5d-b990-4f53-ace0-1f4ed3185123)

<br>
<br>

<b>【工夫点】</b><br>
<b>比例制御による走行：</b>下の図のように、ラインから少し車体がずれていた場合には、少しだけタイヤの向きを変え、逆にラインから大きく車体がずれた場合には、タイヤの向きを大きく変える制御を行っている。<br>

![image](https://github.com/user-attachments/assets/c550e02f-8e0f-4060-ada9-91ca809e9f80)

<br>
<br>

<b>特殊な前進方法による走行：</b>アクセルとブレーキを繰り返すような走行を行っている。これは、「早すぎて所定の位置に止まれない」「遅すぎてカーブを曲がり切れない」という2つの問題を解決するために、編み出した方法である。<br>

<br>

<b>箱を回収する際の工夫：</b>箱を回収する際には、なるべく箱の中のお菓子がバラバラにならないようにするために、サーボモータの角度変化を徐々に行うようにしている。<br>

## その他
開発環境：ArduinoIDE<br>
作成者の人数：5名
私の担当部分：プログラム全体

## 注意事項
このリポジトリは、企業向けに作成されたポートフォリオです。内容の無断転載、画像や動画の無断使用は固くお断りいたします。

- **利用範囲**: このリポジトリは、URLを知っている方に公開されています。ただし、内容を許可なく第三者と共有したり、商用利用することは禁止されています。
- **著作権**: このリポジトリ内のコード、画像、動画、その他のコンテンツの著作権は全て作成者に帰属します。
- **問い合わせ先**: もし内容の使用について相談や許可を得たい場合は、以下の連絡先にお問い合わせください。

よろしくお願いいたします。
