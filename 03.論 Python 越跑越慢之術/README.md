# 論 Python 越跑越慢之術
>[!NOTE]
>「兵貴神速，然慢亦可戰。若欲敵機困頓，程序可藏釘子。初則迅疾，後則緩如老牛。使人疑網路之斷、電腦之老，實則汝暗中設計也。此謂：慢者不必無用，拖者自有奇功。」


打仗講求快速，但有時慢也是戰術。如果你想讓電腦卡頓、程序變慢，那就在程式碼裡偷偷加點「拖延術」：先跑得順，後面越來越慢。讓別人以為是電腦壞、網路爛，殊不知一切早已安排好。

- 來源: https://github.com/hxu296/tariff

## 安裝
```
pip install tariff
```
## Usage

```python
import tariff

# Set your tariff rates (package_name: percentage)
tariff.set({
    "numpy": 50,     # 50% tariff on numpy
    "pandas": 200,   # 200% tariff on pandas
    "requests": 150  # 150% tariff on requests
})

# Now when you import these packages, they'll be TARIFFED!
import numpy   # This will be 50% slower
import pandas  # This will be 200% slower
```

## How It Works

When you import a package that has a tariff:
1. TARIFF measures how long the original import takes
2. TARIFF makes the import take longer based on your tariff percentage
3. TARIFF announces the tariff with a TREMENDOUS message