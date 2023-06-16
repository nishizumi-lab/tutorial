# 【電験3種・電力】新エネルギー発電所に関する試験問題対策

## 新エネルギー発電所の種別

- *太陽電池発電*
    - 太陽電池の光電効果を利用して太陽光エネルギーを電気エネルギーに変換する。
    - 地球に降り注ぐ太陽光エネルギーは、**$1m^2$当たり1秒間に約1kJ**に相当する。
    - 太陽電池の基本単位はセルと呼ばれ、**直流電圧1V程度**が発生するため、これを直列に接続して電圧を高めている。
    - 太陽電池を系統に接続する際は**PCS(パワーコンディショナー)**により交流の電力に変換し、系統に接続する。
    - 一部に地域では太陽光発電の普及によって**日中**に電力の余剰が発生しており、余剰電力は揚水発電の揚水に使われているほか、大容量蓄電池への電力貯蔵に活用されている。
    - PCSに内蔵される連系保護装置で、電気事業者の配電線に連系して悪影響を及ぼさないようにしたり、系統停電時などに電力の供給を停止する
    - 太陽電池の変換効率は太陽電池の種類は、**約15〜20[％]程度**
    - 太陽光発電を導入する際、その地域の年間発電電力量(**設置する方位や傾斜**により変動)を予想することが必要
- *風力発電*
    - 風のエネルギーによって風車で発電機を駆動し発電を行う。
    - 発電機には、同期発電機、久磁石式発電機、誘導発電機が用いられる(大形の風力発電機は、同期発電機又は誘導発電機が使われている)
    - 風力発電所の出力は、エネルギー損失を無視すると、**風速の３乗**に比例。
    - 風車の受風面積をA[m2]、風速をv[m／s] とすると、単位時間当たりの出力P[W]は以下のようになる。
        - $ P=\frac{1}{2}\ro Av^3 $ 
    - 出力Pの導出について、単位時間当たりに通過する風の体積V$[m^3/s]$は$V=Av[m^3/s]$となるので、単位時間当たりに通過する風の質量m[kg/m3] は，空気の密度をρ[kg/m3] とすると，$m = \rho V = \rho Av$となる。物体の運動エネルギーE(=風車の出力)は$E=\frac{1}{2}mv^2=\frac{1}{2} \rho A v^3$となる。
- *洋上風力発電*
    - 陸上の系統の接続では、海底ケーブルによる直流送電が用いられることがある誘電損を考慮しなくて良い利点がある)。
- *小水力発電*
    - 河川や用水路などでの**流込み式発電**が用いられる場合が多い。
- *燃料電池発電*
    - **水素と酸素との発熱反応で**直流の電力を発生させる。負荷変動に対する応答が早い。
    - 化学反応で発生する熱は給湯などに利用できる(代表的な製品はエネファームなど)。
- *地熱発電*
    - 地下から取り出した**蒸気**によってタービンを回して発電する方式。
    - 発電に適した地熱資源は**火山地域**に多く存在する。
- *バイオマス発電*
    - 植物や動物が生成・排出する有機物から得られる燃料を利用する発電方式である。
    - 燃料の代表的なものには、**さとうきびから得られるエタノール**、**木くずから作られる固形化燃料**や、**家畜の糞から作られる気体燃料(メタンガスなど)**がある。
- *分散型電源*
    - 分散型電源からの逆潮流による系統電圧上昇を抑制する手段として、分散型電源の出力抑制や、電圧調整器を用いた電圧の制御などが行われる。

## 参考動画

初心者向け電験三種・電力・16・その他の発電・太陽光・風力・地熱・燃料電池・バイオマス・廃棄物【超簡単に学ぶ！】第三種電気主任技術者
 [![](https://img.youtube.com/vi/_5Px6t7VJJQ/0.jpg)](https://www.youtube.com/watch?v=_5Px6t7VJJQ)


## 【例題1】風力発電のロータ軸出力

【*問題*】
ロータ半径が30mの風車(パワー係数が50％)が、風速10m/sの風を受けるとき、風車のロータ軸出力[kW]を計算せよ。ここで、空気の密度を1.2[kg/m3]とする。
※パワー係数・・・単位時間当たりにロータを通過する風のエネルギーのうちで、風車が風から取り出せるエネルギーの割合

【*解答*】
- 風車の受風面積Aは以下のようになる。
    - $A=\pi r^2=2827.4 [m^2]$
- よって風車のロータ軸出力Pは以下のようになる。
    - $=\frac{1}{2}\rho A v^3=\frac{1}{2}1.2\cdot 2827.4 \cdot 1000 = 1700[kW]$
- ただし、パワー係数が50％なので、0.5Pの「850kW」が答え。



## 関連リンク

- [電験3種試験対策トップページ](../index.md)
- [トップページ](../../../index.md)