# SLAM 中的几何与学习方法 

近年来，深度学习在更高层级的视觉任务中取得瞩目的成绩，如:物体识别,语义分割等。这些课题曾是传统视觉无法或很难解决的任务。深度学习方法的这种能力拓展了我们对视觉任务的想象空间，越来越多的 SLAM 开始在他们的框架中通过融合学习的方法来改进位姿估计的准确程度和环境重建的效果。但是深度学习是一个非常宽广的领域,和 SLAM 相关的课题只是它的一个分支，本书稿将会挑选、聚焦与 SLAM 相关的深度学习任务，希望能通过这本书稿来介绍SLAM 系统中使用的几何和深度学习的方法，帮助读者掌握最新的进展。

![pipeline_glslam](images/pipeline_glslam.png)

## 更新说明

~~目标是每周更新一次，2020年12月完成书稿第一轮的写作。当前更新会陆续将我关注/参与的最新文章写到书中，目录中的章节也会随着内容的完善而不断调整，后面每章内容对应的代码也会整理到这个repo中。
时隔5个月，写了50千字左右，还有很多很多坑没有填上。~~

~~12月前，还有ICRA和CVPR要投稿。我们只能调整目标了，争取12月前，我们可以一起写到100页。~~

3月有中下旬，计划做一个快速的写作。

朋友们，你们如果对书稿有修改意见，不要忘记提issue或发邮件哦。文件过大，**github**无法正常显示，请下载。

| 章节 | 更新内容                                                     |  日期  | 备注 |
| ---- | ------------------------------------------------------------ | :----: | ---: |
|      |                                                              |        |      |
|      | tracking中对极几何与PnP，bundle adjustment, 目标方程与解算，normal prediction，几何特征提取，MLP分类，hello slam，pnp，sparse mapping |  五月  | 2020 |
| 6.2  | dense mapping，增加内容 sparse mapping，vanishing point，decoupling 6D pose，完善内容，经典网络回顾 |  六月  |      |
| 3.2  | 优化器与学习率                                               |  七月  |      |
|      | fix bugs                                                     |  八月  |      |
| 2.1  | RANSAC，structure-slam(深度SLAM 框架)，图网络简介， 图网络层的实现原理，orb 特征方法 | 九月22 |      |
| 1    | 重写第一章                                                   |  十月  |      |
| 2    | hello SLAM, 框架介绍                                         | 11.02  |      |
| 3    | 特征之间的约束                                               | 11.18  |      |
| 12.3 | 优化中的特征描述                                             |  1月   | 2021 |
| 9.2  | TSDF重建                                                     |  2.27  |      |
## 改善书稿质量

如果你在阅读材料的过程中发现问题，请在这里提交一个issue，我可以继续修改它。

如果你有问题/建议，请给我发邮件：yanyan.li@pku.edu.cn, 主题带有 “GL-SLAM书稿”。

## 不忘与回响

如果你想通过微信小额捐助来支持书稿的创作，我将十分感谢。感谢你的不忘，盐粒必有回响。

![wechat_pay](images/wechat_pay.png)

| 日期       | From 盐粒                           |
| ---------- | ----------------------------------- |
| 02.06.2020 | *染，感谢你的支持                   |
| 10.06.2020 | *晨， 感谢你的鼓励                  |
| 29.06.2020 | B*I, 也感谢你的关注                 |
| 03.07.2020 | *秋，感谢鼓励，一起加油             |
| 10.08.2020 | *冬，感谢朋友支持                   |
| 29.09.2020 | *帆，感谢鼓励，祝你科研工作一帆风顺 |
| 24.10.2020 | *吉，感谢支持，欢迎邮件交流         |
| 13.01.2021 | *宸, 感谢你支持我们继续输出         |
| 31.01.2021 | 陈*)， 一起加油，欢迎交流           |


## 版权声明

本项目遵循 “署名-非商业性使用-相同方式共享 4.0 国际 (CC BY-NC-SA 4.0)” 协议。这是一份普通人可以理解的[许可协议](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.zh-Hans)概要 (但不是替代) 。 [免责声明](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh#).

您可以自由地：

- **共享** — 在任何媒介以任何形式复制、发行本作品
- **演绎** — 修改、转换或以本作品为基础进行创作

只要你遵守许可协议条款，许可人就无法收回你的这些权利。 惟须遵守下列条件：

- **署名** — 您必须给出[适当的署名](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh#)，提供指向本许可协议的链接，同时[标明是否（对原始作品）作了修改](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh#)。您可以用任何合理的方式来署名，但是不得以任何方式暗示许可人为您或您的使用背书。
- **非商业性使用** — 您不得将本作品用于[商业目的](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh#)。
- **相同方式共享** — 如果您再混合、转换或者基于本作品进行创作，您必须基于[与原先许可协议相同的许可协议](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh#) 分发您贡献的作品。
- **没有附加限制** — 您不得适用法律术语或者 [技术措施](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh#) 从而限制其他人做许可协议允许的事情。

## 作者相关论文

**Bundle adjustment method using sparse BFGS solution**, Remote Sensing Letter 

**Structure-SLAM: Low-Drift Monocular SLAM in Indoor Environments**, Robotics Automation Letter

**Co-Planar Parametrization for Stereo-SLAM and Visual-Inertial Odometry**, Robotics Automation Letter

**RGB-D SLAM with Structural Regularities**,  arXiv



