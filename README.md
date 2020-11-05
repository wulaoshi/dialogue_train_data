# dialogue_train_data
基于知识库的对话系统，训练数据，已经初步处理，可以直接食用。
## 介绍
- 本项目提供了一个基于知识库的对话系统的训练数据。
- 该数据是已经经过清洗、处理和构造，能直接用于训练“主题模型”，“知识匹配模型”和“”对话生成模型。
- 上述模型详见论文 [Key Factors of Knowledge-driven Conversation System](www.baidu.com)。

## 样例
```
{'history_utt': ['知道重庆森林这部电影吗？'], 'response': '知道呀，是一部由王家卫导演的片子', 'knowledge': '群众类型剧情', 'label': 0, 'mention': -100}
{'history_utt': ['知道重庆森林这部电影吗？'], 'response': '知道呀，是一部由王家卫导演的片子', 'knowledge': 'Crash类型剧情', 'label': 0, 'mention': -100}
{'history_utt': ['知道重庆森林这部电影吗？', '知道呀，是一部由王家卫导演的片子'], 'response': '而主演里更是有王菲，一上映便受到追捧', 'knowledge': '重庆森林主演王菲', 'label': 1, 'mention': '重庆森林'}
{'history_utt': ['知道重庆森林这部电影吗？', '知道呀，是一部由王家卫导演的片子'], 'response': '而主演里更是有王菲，一上映便受到追捧', 'knowledge': '重庆森林类型剧情，文艺', 'label': 0, 'mention': -100}
```
#### 说明
**history_utt**：为对话历史。

**response**：下一句的合适回复。

**knowledge**：候选知识。

**label**：*0* 表示该条候选知识为负样本；*1* 表示该候选知识为正样本。

**mention**：对话主题，当为 *-100*，表示候选知识不正确，故不需要主题。

## 原始数据来源。
- 原始数据为 [KdConv](https://github.com/thu-coai/KdConv)，更多数据的详细信息请见该描述
- 若有侵权，请联系作者删除。
