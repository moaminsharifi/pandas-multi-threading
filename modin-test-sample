# pandas vs modin in read_csv
[datasets](https://www.kaggle.com/skihikingkevin/csgo-matchmaking-damage)

### system:
- i5-6400
- 24gb ram 2400mhz
- samsung 860 evo ssd
- gtx 10603gb


```python
import time
```


```python

import pandas as pd

s = time.time()
esea_master_dmg_demos_1 = pd.read_csv("esea_master_dmg_demos.part1.csv")
esea_master_dmg_demos_2 = pd.read_csv("esea_master_dmg_demos.part2.csv")

esea_master_grenades_demos_1 = pd.read_csv("esea_master_grenades_demos.part1.csv")
esea_master_grenades_demos_2 = pd.read_csv("esea_master_grenades_demos.part2.csv")

e = time.time()
print("Pandas Loading Time = {}".format(e-s))


```

    Pandas Loading Time = 40.80513954162598



```python

del esea_master_dmg_demos_1
del esea_master_dmg_demos_2 

del esea_master_grenades_demos_1
del esea_master_grenades_demos_2

```


```python

import modin.pandas as pd

s = time.time()
esea_master_dmg_demos_1 = pd.read_csv("esea_master_dmg_demos.part1.csv")
esea_master_dmg_demos_2 = pd.read_csv("esea_master_dmg_demos.part2.csv")

esea_master_grenades_demos_1 = pd.read_csv("esea_master_grenades_demos.part1.csv")
esea_master_grenades_demos_2 = pd.read_csv("esea_master_grenades_demos.part2.csv")
e = time.time()

print("Modin Loading Time = {}".format(e-s))
```

    Modin Loading Time = 18.163443565368652




###  for 14 time single file esea_master_dmg_demos.part1.csv
    - pandas 16.57640128476279
    - modin 7.358242324420384
