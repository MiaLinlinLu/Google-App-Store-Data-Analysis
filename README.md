# Google-App-Store-Data-Analysis
概览
Google Play Store（Google Play商店）是谷歌官方的软件应用商店，拥有上架软件数十万款，下载量更是突破了20亿次，为了手机用户提供了极为广泛的应用选择，很受大家的欢迎。我们提供了 Google Play 商店中一些 App 的数据，你的任务是对这个数据进行探索，通过数据分析的方式发现有趣的洞察。你可以先自己提出感兴趣的问题，并利用已有的数据进行分析，通过调用本课中学到的数据分析常用函数，来计算数据中的统计数据和让数据可视化，并得出结论。

项目任务
应提交 ipynb 格式和 html 格式的文件。在本项目中，你需要完成下面完成的任务：

提出感兴趣的问题
对数据进行评估和清理
对数据集进行探索性分析
对数据可视化
得出结论

## 实际数据清理包括：
1. 修改列名，统一同一变量的不同写法（大小写、空格等）
2. 查看各列空值占比，填充空值。
3. 清楚重复值
4. 改变变量的数据类型
5. bar图、直方图展示数据
6. 按照某列对data frame进行排序

## 问题：最受欢迎的APP是什么类型？

## 探索分析
1. 统计各个category的app的平均rating(评分)。
  直方图中，可以看出，共有5个categories 的平均评分超过了4分，找出这5类category。前5类分别为： Education, art and design, entertainment, game, comics
2. 统计下载量前5名类别分别是： communication, social, video_players, productivity, photography
3. 统计reviews的前5名，前5名类别分别是： social, communication, game, photography, video_players
4. 前5名 `评分`、`下载量`、`评论数` 三个指标，没有一个是三者共同的类别
- 其中 `game` 是 评分前5名中 唯一 和 评论数前5名重复的类别, 再次查看installs的排名，发现game的下载量`installs`排在第6位。

## 结论
1. 评分前5名的类别是 `Education`, `art and design`, `entertainment`, `game`, `comics`
2. 下载量前5名的类别是：`communication`, `social`, `video_players`, `productivity`, `photography`
   另外，`game`排第6位
3. 评论数前5名类别分别是： `social`, `communication`, `game`, `photography`, `video_players`
4. 结论：
    - 评分、下载量和评论数 均靠前的 类别是： `Game`，是最受欢迎的APP类型
    - 下载量 和 评论数 多的 APP类别 并没有对应很高的评分，但是两者的前5名有4项重合。说明用户下载量和评论数有可能是相关的。可后续进一步分析。
    - 评分前5名的类别中 只有4类下载量和评论数也很高。说明高评分不代表受众广。
    
5. 延伸
- 分析中，尝试根据 评分、下载量和评论数 来找出最受欢迎的APP类别。该分析中，抽取了各指标的前5名来进行考虑，可以做更多的比如前10名。
- 如果数据集再包含用户使用频次，将有助于更好地找出最受欢迎app类别。
