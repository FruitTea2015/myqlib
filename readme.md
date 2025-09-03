运行说明：

需要先下载默认数据，再运行代码文件。

下载默认数据：

CN:
```
# get 1d data
python -m qlib.cli.data qlib_data --target_dir ./qlib_data/cn_data --region cn

# get 1min data
python -m qlib.cli.data qlib_data --target_dir ./qlib_data/cn_data_1min --region cn --interval 1min
```
US: 
```
# get 1d data
python -m qlib.cli.data qlib_data --target_dir ./qlib_data/us_data --region us

# get 1min data
python -m qlib.cli.data qlib_data --target_dir ./qlib_data/us_data_1min --region us --interval 1min
```

下一步的计划：
1. 换成默认的美股数据（1min）
2. 换成默认的alpha360因子库
3. 换成其他模型（xgboost、catboost、MLP）
4. 换成其他策略（除了TopKDropout之外看看其他策略）
5. 自己从聚宽、yfinance下载数据并导入运行
6. 自定义因子
7. 更改策略，加上止损功能
8. RD-Agent配合，遗传算法挖掘量价因子