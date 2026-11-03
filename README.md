# 基于SpringBoot+Vue的档案管理系统

![Spring Boot](https://img.shields.io/badge/-Spring%20Boot-6DB33F?style=flat-square&logo=spring-boot&logoColor=white) ![Vue3](https://img.shields.io/badge/-Vue3-grey?style=flat-square) ![MySQL](https://img.shields.io/badge/-MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![MyBatis](https://img.shields.io/badge/-MyBatis-000000?style=flat-square&logo=mybatis&logoColor=white) 

## 项目介绍

本系统是一款面向党政机关、企事业单位与高校档案馆场景的智慧数字档案全生命周期管理平台，针对纸质查阅繁琐、案卷著录标准不统一、数字化原文权限分级不清、实体库房储位难追踪、借阅归还缺少闭环审批、满期鉴定销毁失控、专题编研展示渠道匮乏等问题，把门类体系、案卷编目、件级著录、原文挂接、借阅审批、库房十防巡检、鉴定销毁、移交征集、编研展览与操作审计整合到同一套前后端分离工程中。

系统采用 SpringBoot + Vue 架构，区分普通查档用户、档案员与系统管理员：用户端支持全馆检索、在线借阅、专题展厅与查档咨询；管理端覆盖著录归档、借阅核销、库房巡检、鉴定销毁、移交征集、编研发布与 ECharts 驾驶舱。借阅审批与实体出库占用可追溯，鉴定销毁按待鉴定→待执行→已销毁闭环，适合作为毕设、课设与数字档案学习参考。

## 主要功能模块

- **用户认证与角色分流**：JWT 鉴权，普通用户进入门户，档案员/管理员进入后台；路由与接口双重隔离
- **馆藏检索与详情**：按关键词、门类、载体多维过滤，查看档号、责任者、密级、保管期限、排架与摘要
- **数字化原文**：件级档案挂接附件，记录 SHA-256，按权限预览/下载
- **在线借阅闭环**：申请电子查阅或实体调阅，待审批/借阅中/驳回/归还/逾期全状态跟踪，可撤回与归还申请
- **专题展厅与政策法规**：浏览编研专题与归档指南，支持置顶与阅读量展示
- **查档咨询**：提交主题与内容，查看待回复/已答复与官方回函
- **工作台驾驶舱**：馆藏件数、案卷、待审借阅、数字化率、库房容量与近月趋势/门类占比等 ECharts 指标
- **档案资源中台**：门类体系、案卷编目、件级著录、原文附件与生命周期审计轨迹
- **借阅利用审批**：准予/驳回、覆写核准天数，借阅中办理归还入库核销
- **实体库房与十防巡检**：库房温湿度与防火/防盗/防潮/防虫安全结论登记
- **鉴定销毁与归集**：延期/降密/依法销毁流程，部门移交验收，社会征集入馆归藏
- **论文与 UML 概览**：配套论文设计实现页拼图与 UML 图列表，便于答辩材料对照

## 技术架构

- **后端**：Spring Boot + MyBatis-Plus + JWT + Lombok
- **前端**：Vue 3 + TypeScript + Vue Router + Pinia + Element Plus + Vite + ECharts
- **数据库**：MySQL

<!-- screenshots-start -->
## 系统截图

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/archivemanage/%E7%99%BB%E5%BD%95%E9%A1%B5%E9%9D%A2.png" alt="登录页面" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/archivemanage/%E7%94%A8%E6%88%B7%E9%A6%96%E9%A1%B5.png" alt="用户首页" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/archivemanage/%E6%A1%A3%E6%A1%88%E6%A3%80%E7%B4%A2.png" alt="档案检索" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/archivemanage/%E6%88%91%E7%9A%84%E5%80%9F%E9%98%85.png" alt="我的借阅" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/archivemanage/%E4%B8%93%E9%A2%98%E5%B1%95%E5%8E%85.png" alt="专题展厅" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/archivemanage/%E7%AE%A1%E7%90%86%E5%91%98%E4%BB%AA%E8%A1%A8%E7%9B%98.png" alt="管理员仪表盘" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/archivemanage/%E6%A1%A3%E6%A1%88%E6%96%87%E4%BB%B6%E7%AE%A1%E7%90%86.png" alt="档案文件管理" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/archivemanage/%E5%80%9F%E9%98%85%E5%AE%A1%E6%89%B9.png" alt="借阅审批" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/archivemanage/%E8%AE%BA%E6%96%87%E5%9B%BE1.png" alt="论文图1" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/archivemanage/%E8%AE%BA%E6%96%87%E5%9B%BE2.png" alt="论文图2" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/archivemanage/UML%E5%9B%BE%E5%88%97%E8%A1%A8.png" alt="UML图列表" width="600" />

<!-- screenshots-end -->

## 接毕业设计和论文

### 作者微信：vvsgxmn  (支持修改、 部署调试、 支持代做毕设)

### 接网站建设、小程序

### 选题+开题报告+任务书+程序定制+安装调试+论文+答辩ppt 都可以做

### 购买地址：[https://www.vvxx.love](https://www.vvxx.love)（vv毕设网）

### 支持 **一键生成 UML 图**：上传项目压缩包即可自动产出功能模块图、用例图、流程图、E-R 图、时序图等全套毕设图表。

### 提供 **免费配套软件下载 + 安装说明 + 部署教程**

![vv毕设网 - 一键画图](https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/uml-draw.png)

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/image-20260825133349317.png" alt="image-20260825133349317" />

⚠️ Bug添加微信**免费修复**，免费修复。其他平台的私信一律不管（微信方便发送文件）
