# dev-ds

### 本文主要介绍对ds调度（基于1.2版本）的几点改造
##### 1.去掉了project的概念,直接进入项目就是运维、管理、监控等；
![运维](https://github.com/hujiang75277381/dev-ds/blob/main/%E8%BF%90%E7%BB%B4-01.png)
##### 2.工作流管理新增了目录；
![工作流定义](https://github.com/hujiang75277381/dev-ds/blob/main/%E5%B7%A5%E4%BD%9C%E6%B5%81%E5%AE%9A%E4%B9%89%E7%AE%A1%E7%90%86.png)
##### 3.工作监控开发了以工作流定义作为维度的展示；
![工作流实例监控](https://github.com/hujiang75277381/dev-ds/blob/main/%E4%BB%BB%E5%8A%A1%E7%9B%91%E6%8E%A7.png)
##### 4.新增了任务计划调度图表,可以具体的查看系统的某一时刻的密集程度；
![工作流实例执行计划](https://github.com/hujiang75277381/dev-ds/blob/main/%E6%89%A7%E8%A1%8C%E8%AE%A1%E5%88%92.png)
##### 5.改造了执行器管理,把填写ip修改为在线执行器的选择；
![执行器分组](https://github.com/hujiang75277381/dev-ds/blob/main/%E6%89%A7%E8%A1%8C%E5%99%A8%E5%88%86%E7%BB%84.png)
##### 6.把执行器的那块逻辑剥离成jar包,提供给执行器实现者使用；
##### 7.将执行器改造为单一的功能,比如调度基础执行器就只能处理 shell、python、依赖、子任务等task类型的任务，元数据采集执行器就只能处理元数据采集任务；
##### 8.将执行器端控制检查系统资源的配置下放到执行器本地配置,新增JVM剩余内存的检查；
