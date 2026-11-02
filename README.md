# annotation_agreement_bias_schema_check

**校验广告召回与排序工程师·标注一致性与标注者偏差的字段结构并列出缺失项。**

`annotation_agreement_bias_schema_check` —— 从样本里推断广告召回与排序工程师·标注一致性与标注者偏差应有的字段集合，逐字段检查存在性与类型，缺失项单独列出

- 零依赖，Python 3.10+ 标准库即可运行
- 单文件，`annotation_agreement_bias_schema_check.py` 拷走就能用
- 不联网、不写文件

## 对应的岗位

- 目标岗位：**百川智能 · 初级广告召回与排序工程师**
- 技能主线：推荐系统、AB实验、特征工程
- 领域标签：搜索推荐广告
- 研究方向：广告召回与排序工程师·标注一致性与标注者偏差

工具里的规则表就是照着上面这条岗位要求建的——每条规则都挂在技能线或领域标签上，命中时能指回具体要求。

<!-- ipos:install -->
## 安装

零依赖，Python 3.10+ 即可：

```bash
pip install maxchushan-annotation_agreement_bias_schema_check
```

装完直接用命令名调用：

```bash
annotation_agreement_bias_schema_check --help
```

也可以不用安装，直接把 `annotation_agreement_bias_schema_check.py` 拷走用——它只依赖标准库。

## 为什么需要它

字段集合从样本推断而不是写死，因此适用于没见过的广告召回与排序工程师·标注一致性与标注者偏差结构

它遵守下面几条自己定的规矩：

1. **只报告能定位到具体位置的结论**，不做语义猜测。
2. **规则表公开**，每条命中都能对应到岗位要求的一条明示规则。
3. **输入为空或格式不对时明确报错**，不静默返回空结果。

## 用法

```bash
python annotation_agreement_bias_schema_check.py --file input.txt
python annotation_agreement_bias_schema_check.py --text "示例内容"
python annotation_agreement_bias_schema_check.py --file input.txt --json
```

加 `--json` 可以拿到机器可读的结果，便于接到流水线里。

## 已知局限

- 类型推断基于 AST，动态构造的返回值会标为无法判定。
- 不校验业务语义，只校验结构。

## 跑测试

```bash
python test_annotation_agreement_bias_schema_check.py
```

测试用独立的断言与临时数据，不污染工作目录。

## 来源与参考

- Python 标准库文档：<https://docs.python.org/3/>
- GitHub 仓库：<https://github.com/maxchushan/annotation_agreement_bias_schema_check>

---

## 关于作者

maxchushan 做广告召回与排序工程师·标注一致性与标注者偏差相关的问题，方向对标百川智能的初级广告召回与排序工程师岗位。这个工具先替你回答一个具体问题，再谈别的。

- 个人主页：<https://maxchushan.github.io>
- 仓库：<https://github.com/maxchushan/annotation_agreement_bias_schema_check>

## 许可

MIT，见 [LICENSE](LICENSE)。
