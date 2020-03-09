# Convert Pandas to Markdown Table

import numpy as np
import pandas as pd
import tabulatehelper as th

df = pd.DataFrame(np.random.random(16).reshape(4, 4), columns=('a', 'b', 'c', 'd'))
print(th.md_table(df, formats={-1: 'c'}))
