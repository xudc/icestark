# 主应用

又称框架应用或基座应用，一个系统只有一个主应用，主应用负责系统整体的 Layout 以及微应用的管理与注册。

主应用应该保持职责明确。一个设计良好的主应用只做两件事情：

1. 系统整体 Layout 的设计

2. 所有微应用的配置与注册


主应用尽量避免包含具体页面的 UI 代码，如果主应用做了过多的事情会带来以下问题：

+ 主应用样式代码太多，会增加微应用和主应用样式冲突概率

+ 主应用为微应用提供其他能力比如一些全局 API，会破坏微应用的独立性，增加相互的耦合

+ 主应用本质是一个中心化的部分，变更后原则上需要回归所有微应用，因此需要保证职责的简单，越简单的东西越稳定