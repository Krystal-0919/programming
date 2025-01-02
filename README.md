## 项目简介

这个项目包含一个ipynb文件，用于执行数据处理和机器学习分析。主要包括逻辑回归、随机森林等机器学习方法的应用。旨在通过实际数据集展示数据预处理、模型训练和评估的典型流程。
## 作者信息

中国人民大学     唐嘉红

邮箱：tangjiahong2021@163.com
## 运行环境

    Python 3.11
    Jupyter Notebook (推荐用于运行和展示代码)

## 使用的主要包

    pandas
    numpy
    statsmodels
    scikit-learn
    matplotlib

## 安装依赖

在Python环境中运行以下命令以安装必要的包：

pip install pandas numpy statsmodels scikit-learn matplotlib plotnine

以上命令用于安装Python包(默认最新版本即可)。
## 程序说明

程序含有类CustomLabelEncoder，初始化时创建了一个 LabelEncoder 的实例。

fit_transform 方法接受一个 DataFrame 作为输入。 

首先检查输入是否为 pandas DataFrame 类型，如果不是，则抛出 ValueError。

创建一个空列表 encoded_columns 用于存储编码后的列。

创建一个空字典 encoding_maps 用于存储每个列的编码映射。

遍历输入 DataFrame 的每一列。如果列的数据类型为浮点数或整数，则直接将该列添加到 encoded_columns 中。

如果列的数据类型不是数值类型，使用 LabelEncoder 对该列进行拟合和转换。

将转换后的列作为新的 Series 对象添加到 encoded_columns 中，并为其指定原始列名。

将每个列的编码映射保存到 encoding_maps 字典中。

使用 pd.concat 将所有编码后的列合并成一个新的 DataFrame。

打印每个列的编码映射。

返回新的编码后的 DataFrame。


## 复现步骤
在jupyter中逐单元格运行即可
