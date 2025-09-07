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

Jupyter Notebook 文件侧重于后面的可视化部分。可视化部分的解释链接：[文档链接](https://qlib.readthedocs.io/en/latest/component/report.html#graphical-reports)


下一步的计划：
1. done 换成默认的美股数据（1min）及多周期数据（1min和1day），设置label
2. 换成默认的alpha360因子库
3. 换成其他模型（xgboost、catboost、MLP）
4. 换成其他策略（除了TopKDropout之外看看其他策略）
5. 自己从聚宽、yfinance下载数据并导入运行
6. done 自定义因子
7. 更改策略，加上止损功能
8. RD-Agent配合，遗传算法挖掘量价因子（也有用DEAP自动挖掘因子）



参考教程：

1. 运行Qlib自带的多个机器学习模型（使用alpha158和alpha360数据集）[链接](https://github.com/microsoft/qlib?tab=readme-ov-file#quant-model-paper-zoo)
2. 自定义数据集（因子+label） [链接](https://qlib.readthedocs.io/en/latest/advanced/alpha.html)
3. 滚动训练以适应市场风格变化 [链接](https://github.com/microsoft/qlib?tab=readme-ov-file#adapting-to-market-dynamics)
4. 多周期（分钟+日频）数据构建数据集：`qlib\examples\benchmarks\LightGBM`目录下有2个文件：`workflow_config_lightgbm_multi_freq.yaml`和`multi_freq_handler.py`