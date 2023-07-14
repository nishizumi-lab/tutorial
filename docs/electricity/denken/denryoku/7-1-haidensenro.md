# 【電験3種・電力】配電線路に関する試験問題対策

## 高圧引込ケーブル

- [ストレスコーン](../07-1-shrink-back-stress-cone.md)
    - 遮蔽銅テープの端部へ電気力線が集中するのを防ぎ(電位傾度を緩和)、絶縁体の絶縁破壊を防止する。


## 単相2線式 配電線路の電圧降下

単相二線式の配電線路では、負荷に対して供給される線路と戻りの線路で電圧降下が発生します。
負荷の力率(遅れ力率)$cos\theta$のとき、回路図とベクトル図は以下のとおり。

![回路](./assets/7-1-2.png) 

$\dot{E}$と$\dot{V}$の位相差が十分に小さいとき、配電線路の電圧降下$\epsiron = E-V$は以下のとおり。

$ E \simeq V+2RIcos\theta + 2XIsin\theta $

$E-V=2RIcos\theta + 2XIsin\theta$

$ \epsilon = 2I(Rcos\theta + Xsin\theta) $

↑ この式は要暗記。

配電線路の線間電圧$V[V]$、線電流$I[A]$、力率$cos\theta$のとき、送電電力$P[W]$は以下のとおり。

$P=VIcos\theta$

↑ この式は要暗記。

## 3相3線式 配電線路の電圧降下

3相3線式の電線路では、荷の力率(遅れ力率)$cos\theta$のとき、一相分の等価回路とベクトル図は以下のようになる。

![回路](./assets/7-1-1.png) 

配電線路の三相分の電圧降下$\epsiron$は以下のとおり。

$ \frac{E}{\sqrt{3}} \simeq \frac{V}{\sqrt{3}}+RIcos\theta + XIsin\theta $

$\frac{E}{\sqrt{3}} - \frac{V}{\sqrt{3}}=RIcos\theta + XIsin\theta$

$ E-V = \sqrt{3}(RIcos\theta + XIsin\theta) $

$ \epsiron = \sqrt{3}(RIcos\theta + XIsin\theta) $

↑最後の式は要暗記。

配電線路の線間電圧$V[V]$、線電流$I[A]$、力率$cos\theta$のとき、送電電力$P[W]$は以下のとおり。

$P=\sqrt{3}VIcos\theta$

↑ この式は要暗記。

## 【例題1】単相２線式配電線路の電圧降下と負荷電流

単相 2 線式の配電線路において、電線 1 線当たりの抵抗と長さは、a−b 間で 0.3 [Ω/km]及び250 [m] 、 b−c 間で 0.9 [Ω/km] 及び100 [m]である。このとき、次の①②の値を計算せよ

①b−c 間の 1 線の電圧降下$v_{bc}$ [V] 及び負荷 B と負荷 C の負荷電流$i_b,  i_c$[A]を求めよ。 
ただし、給電点 a の線間の電圧値と負荷点 c の線間の電圧値の差を 12.0 [V] とし， a−b 間の 1 線の電圧降下 𝑣ab=3.75 [V] とする。 負荷の力率はいずれも 100 [％] 、線路リアクタンスは無視するものとする。

②　次に、図の配電線路で抵抗に加えて a−c 間の往復線路のリアクタンスを考慮する。
このリアクタンスを 0.1 [Ω] とし、 b 点には無負荷で$i_b=0$ [A] ， c点には受電電圧が 100 [V] 、遅れ力率0.8、1.5 [kW] の負荷が接続されているものとする。
　このとき、給電点 a の線間の電圧値と負荷点 c の線間の電圧値 [V] の差を計算せよ。

## 参考動画

初心者向け電験三種・電力・9・汽力発電・効率【超簡単に学ぶ！】第三種電気主任技術者
 [![](https://img.youtube.com/vi/OseY2IeapXI/0.jpg)](https://www.youtube.com/watch?v=OseY2IeapXI)

【カフェジカ実験室】穴あきケーブルに、高電圧メガをあててみた！
 [![](https://img.youtube.com/vi/hCkMR5C_z6Q/0.jpg)](https://www.youtube.com/watch?v=hCkMR5C_z6Q)

 ## 関連リンク

- [電験3種試験対策トップページ](../index.md)
- [トップページ](../../../index.md)