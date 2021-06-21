空き領域の数をN,確保済み領域をMをする。

# First-fit

| Challenge | Time | Utilization |
| --------- | ---- | ----------- |
|     1     | 7ms  |   70%       |
|     2     | 7ms  |   40%       |
|     3     | 132ms|  7%         |
|     4     | 24359ms| 15%       |
|     5     | 17415ms| 15%       |

# Best-fit

| Challenge | Time | Utilization |
| --------- | ---- | ----------- |
|     1     | 1539ms  |   70%       |
|     2     | 670ms  |   40%       |
|     3     | 885ms|  50%         |
|     4     | 9001ms| 71%       |
|     5     | 5728ms| 74%       |

First-fitと比べると速度は落ちるが，メモリを効率よく分配できていることがわかる。最適な空き領域を選ぶ際に，全ての空き領域を見る必要があるためその分時間がかかってしまう。（時間量はO(N)）

ALEX_COMMENT:  in order to avoid searching all every time, how about keeping the free-list always sorted?
               maybe with that you could do binary-search instead?

# Worst-fit

| Challenge | Time | Utilization |
| --------- | ---- | ----------- |
|     1     | 1413ms  |   70%       |
|     2     | 636ms  |   40%       |
|     3     | 51677ms|  4%         |
|     4     | 529300ms| 7%       |
|     5     | 489782ms| 7%       |

First-fitと比べると速度もメモリ効率も落ちていることがわかる。
