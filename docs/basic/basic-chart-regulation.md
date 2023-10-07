# 基础篇 - 音符的种类和说明

## TAP

![TAP](imgs/note-tap.png)

* 最基本的音符。

* 可以放置的音符宽度为 <span style="color:red"> 1, 2, 3, 4, 6, 8, 16 </span>

## ExTAP

![ExTap](imgs/note-extap.png)

* 必定获得最高判定 (JUSTICE CRITICAL) 的 TAP 音符。

* 可以放置的音符宽度为 <span style="color:red"> 1, 2, 3, 4, 6, 8, 16 </span>

## FLICK

![FLICK](imgs/note-flick.png)

* 需要快速向左或右滑动的音符。

* **只在 MASTER 和 ULTIMA 难度出现。**

* 可以放置的音符宽度为 <span style="color:red"> 1, 2, 3, 4, 6, 8, 16 </span>

## DAMAGE

![DAMAGE](imgs/note-damage.png)

* 碰到后会产生 MISS 判定的地雷音符。不碰则会获得最高判定 (JUSTICE CRITICAL)。

* **只在 WORLD’S END 难度出现。普通难度请不要使用。**

* 可以放置的音符宽度为 <span style="color:red"> 1, 2, 3, 4, 6, 8, 16 </span>

## HOLD

![HOLD](imgs/note-hold.png)

* 需要持续按到终点的音符。

* 可以放置的音符宽度为 <span style="color:red"> 1, 2, 3, 4, 6, 8, 16 </span>

## SLIDE

![SLIDE](imgs/note-slide.png)

* 按照轨迹滑动到终点的音符。

* 可以放置的音符宽度为：

  * 起点、终点: <span style="color:red"> 1, 2, 3, 4, 6, 8, 16 </span>

  * 中继点、控制点: <span style="color:red"> 1, 2, 3, 4, **5**, 6, 8, **10**, **12**, **14**, 16 </span>

![Examples](imgs/reg-slide.png)

> *官方谱面中存在少许个例*

## AIR

![AIR](imgs/note-air.png)

* 挥动手臂往上 (AIR-UP) 或往下 (AIR-DOWN) 的音符。

* 可以放在 TAP、ExTAP、FLICK、DAMAGE 或 HOLD 和 SLIDE 的终点上。

* **只有在 WORLD'S END 难度才能使用颜色反转的 AIR。**

* 可以放置的音符宽度为：<span style="color:red"> 1, 2, 3, 4, 6, 8, 16 </span>

## AIR-HOLD

![AIR-HOLD](imgs/note-airhold.png)

* 向上挥动手臂 (AIR-ACTION) 并保持到终点，在中继点和终点也需要挥动手臂 (AIR-ACTION) 的音符。

* 终点的音符可以删除。

    ![没有终点的AIR-HOLD](imgs/example/air-no-end.png)

* 可以设置 AIR 颜色反转和 AIR-HOLD 高度。

    ![不同高度的AIR-HOLD](imgs/example/air-example1.png)

* 可以放置的音符宽度为：<span style="color:red"> 1, 2, 3, 4, 6, 8, 16 </span>

## AIR-SLIDE

![AIR-SLIDE](imgs/note-airslide.png)

* 向上挥动手臂 (AIR-ACTION) 并保持到终点，在中继点和终点也需要挥动手臂 (AIR-ACTION) 的音符。

* 判定和 AIR-HOLD 一样。

* 终点的音符可以删除。

* 可以设置 AIR 颜色反转和 AIR-HOLD 高度。

    ![不同高度的AIR-SLIDE](imgs/example/air-example2.png)

* 可以放置的音符宽度为：

  * 起点、中继点、终点: <span style="color:red"> 1, 2, 3, 4, 6, 8, 16 </span>

  * 控制点: <span style="color:red"> 1, 2, 3, 4, **5**, 6, 8, **10**, **12**, **14**, 16 </span>

## AIR-CRUSH

![AIR-CRUSH](imgs/note-aircrush.png)

* 起点、中继点、终点需要挥动手臂 (AIR-CRUSH ACTION) 的音符。中间的线只是装饰，没有判定。

* 终点的音符可以删除。

* <div class="rainbow-text" style="text-align: left;"> <span class="block-line"><span><span style="color:#ff0000;">装</span><span style="color:#ff8c00;">饰</span><span style="color:#ffd700;">线</span><span style="color:#59ff00;">的</span><span style="color:#00ff2f;">颜</span><span style="color:#00ffbb;">色</span><span style="color:#00b7ff;">可</span><span style="color:#002bff;">以</span><span style="color:#5e00ff;">改</span><span style="color:#ea00ff;">变</span><span style="color:#ff0088;">。</span></span></span> </div>

* 可以放置的音符宽度为：
  * 起点、终点: <span style="color:red"> 1, 2, 3, 4, **5**, 6, 8, **10**, **12**, **14**, 16 </span>

## AIR-TRACE

![air trace](imgs/note-airtrace.png)

* 只是装饰线，并没有任何判定 (AIR-CRUSH ACTION) 的音符。

* <div class="rainbow-text" style="text-align: left;"> <span class="block-line"><span><span style="color:#ff0000;">装</span><span style="color:#ff8c00;">饰</span><span style="color:#ffd700;">线</span><span style="color:#59ff00;">的</span><span style="color:#00ff2f;">颜</span><span style="color:#00ffbb;">色</span><span style="color:#00b7ff;">可</span><span style="color:#002bff;">以</span><span style="color:#5e00ff;">改</span><span style="color:#ea00ff;">变</span><span style="color:#ff0088;">。</span></span></span> </div>

* **本质上是没有终点、起点、以及控制点的AIR-CRUSH**

## ExSLIDE，ExHOLD

![ex slide](imgs/note-exslide.png)

* 在[谱面属性设定](docs/basic/basic-export#step1-谱面属性设定)中启用 **Join ExTAP to SLIDE or HOLD BEGIN** 来使用。

* 在起点上叠加一个 ExTAP 来表示 ExSlide。

  * 如果上述设定未启用， TAP 和 ExTAP 就只会是单纯叠在一起而已。

* 如果想在起点上添加 AIR，就需要另外叠加一个 ExTAP ，并在这个ExTap上添加Air。

  * 也就是说，起点、ExTAP、带有 AIR 的 ExTAP 这**三个音符**会叠在一起。
  
    ![exslide air](imgs/example/exslide-air.png)

* **另外只要有一个 ExTAP 叠加，所有相同起点的判定都会变成 ExTAP 式的。**

  * 因此没有必要叠加多个 ExTap
  * 
    *（图中有两个相同的起点和一个ExTap相互叠加）*
    ![two exslide](imgs/example/exslide-example.png)

    
