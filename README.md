# 规范Git Commit

# commit message格式
```bash
<type>(<scope>): <subject># 冒号用英文并且后面空一格(也是英文，即半角空格)
# 空一行
(<body>)
# 空一行
(<footer>)
```
## type(必须)

用于说明git commit的类别，通常使用以下的标识：

- feat：新功能(feature)；
- fix/to：bug修复
   - fix：产生diff，并修复bug，通常用于一次提交直接修复bug；
   - to：产生diff，但并没有修复bug，通常用于多次提交，最终修复bug的时候，需使用fix；
- docs：文档(documentation)；
- style：代码格式或排版；
- refactor：重构(既没有增加功能，也没有修复bug的代码变动)；
- perf：优化，比如：性能或体验；
- test：增加测试；
- chore：构建过程或辅助工具的变动；
- revert：回滚到上一个版本；
- merge：代码合并；
- sync：同步主线或分支的Bug；

## scope(可选)
用于说明commit影响的范围，比如：数据层、业务层、控制层、视图层，或者是用户，功能模块等；

- 如没有特殊需求，建议使用小写横杠连接英文单词；如：language-service

## subject(必须)
对commit目的的简短描述，一般不超过50个字符：

- 建议使用中文（感觉中国人用中文描述问题能更清楚一些）；
- 结尾不加句号或其他标点符号；

## body(可选)
对commit目的的详细描述，可以分成多行：

- 应该说明代码变动的动机，以及与以前行为的对比·

## footer(可选)
对禅道上解决的Bug，或者完成的任务进行描述（直接填写Bug或者任务的编码即可）

- 解决Bug

#### 示例：
- 解决Bug
```bash
Resolves #123, #245, #992
```

- 完成任务
```bash
Done #234, #456
```

# 总结
根据以上规范 git commit message 将是如下的格式：

```bash
fix(user-service): 用户查询缺少username属性

Resolves #123, #456
```

```bash
feat(controller): 用户查询接口开发

增加系统基础档案员工及账号管理及登录相关功能所使用的接口；

Done #999, #888
```



以上就是我们梳理的git commit规范，那么我们这样规范git commit到底有哪些好处呢？

- 便于程序员对提交历史进行追溯，了解发生了什么情况；
- 一旦约束了commit message，意味着我们将慎重的进行每一次提交，不能再一股脑的把各种各样的改动都放在一个git commit里面，这样一来整个代码改动的历史也将更加清晰；
- 格式化的commit message才可以用于自动化输出Change log；



