# pandas-pipeline (WIP)

Organize your pipelines

Install

```bash
pip install git+https://github.com/remykarem/pandas-pipeline#egg=pandas-pipeline
```

Firstl, import

```python
import pandas_pipeline
```

such that the `.pipeline` will be available to your DataFrame objects. 

Familiar API

* as_type: convert the types of multiple columns
* apply: perform apply on multiple series objects
* map: perform map on multiple columns
* fillna

New

* sapply: perform vectorised operations on multiple series
* dapply
* drop_duplicate_columns
* drop_columns_with_rules
* map_categorical_binning
* map_numerical_binning

## `.pipeline.astype`

Instead of

```python
df["age"] = df["age"].astype(int)
df["weight_new"] = df["weight"].astype("category")
```

do

```python
df = df.pipeline.astype({
    "age": int,
    ("weight_new", "weight"): "category"
})
```

```python
df = df.pipeline.apply({
})
```

```python
df = df.pipeline.sapply({
})
```

```python
df = df.pipeline.map({
})
```

```python
df = df.pipeline.fillna({
})
```
