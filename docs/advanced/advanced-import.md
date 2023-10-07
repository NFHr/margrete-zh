# SUS 譜面や UGC 譜面を取り込む
シミュレーター用として出力された SUS (Seaurchin Score) 形式の譜面や UGC (UMIGURI Chart) 形式の譜面を取り込んで編集することができます。

## 方法
1. メニューの **ファイル** > **他形式譜面取り込み** をクリックします。
2. 取り込みたい譜面を選択します。
3. 取り込まれました。

## 対応状況
### SUS (Seaurchin Score) 形式
|                                      |   |
|:------------------------------------:|:----:|
| `#TITLE`                             | ✔ |
| `#SUBTITLE`                          | ❌ |
| `#ARTIST`                           | ✔ |
| `#GENRE`                            | ❌ |
| `#DESIGNER`                         | ✔ |
| `#DEFFICULTY`                        | ✔ |
| `#PLAYLEVEL`                         | ✔ |
| `#SONGID`                            | ✔ |
| `#WAVE`                              | ✔ |
| `#WAVEOFFSET`                        | ✔ |
| `#JACKET`                            | ✔ |
| `#BACKGROUND`                        | ✔ |
| `#MOVIE`                             | ❌ |
| `#MOVIEOFFSET`                       | ❌ |
| `#BASEBPM`                           | ❌ |
| `#REQUEST`                           | ✔ |
| `#ATR`, `#ATTRIBUTE`, `#NOATTRIBUTE` | ❌ |
| `#TIL`, `#HISPEED`                   | ✔ |
| `#NOSPEED`                           | ❌ |
| `#MEASUREBS` | ✔ |
| `#MEASUREHS` | ✔ |
| ノーツ定義 | ✔ |
| `#REQUEST ticks_per_beat` | ✔ |
| `#REQUEST metronome` | ✔ |
| `#REQUEST enable_priority` | ❌ |
| `#REQUEST enable_moving_lane` | ❌ |
| `#REQUEST segments_per_second` | ❌ |

### UGC (UMIGURI Chart) 形式
* Version 3.0 の全てに対応。
