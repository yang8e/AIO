# AIO
## 工具描述
`主要是针对目前常见的外网渗透工具进行半自动化集合，用来快速打点渗透。`
## 主要功能
```
目前集成了四块功能，fofa搜索、fscan 扫描、nuclei扫描、rustscan扫描,还有就是漏洞利用，目前只有swagger利用，自动对api进行扫描查找未授权接口。
每个工具都可单独使用，也可集合使用，集合使用主要是基于fofa结果或者rustscan结果进行渗透。
整个工具流程串起来是基于项目制的，就是选择同一项目即可半自动化渗透。
```
## 渗透思路
```
设想的主要工作流程为
对一个公司进行渗透，利用fofa扫描出资产列表-〉利用rustscan全端口扫描-〉得到资产合集，利用fscan对常见的漏洞扫描-〉得到结果
nuclei主要是针对暴露出0day或者1day，利用fofa测绘，然后进行扫描利用。
```
## 注意事项
```
1、需要在config.properties中添加fofa api认证信息
2、rustscan 是需要在远程服务器中部署的，ssh信息需要在config.properties添加
3、nuclei yaml文件在nuclei/POC 中，需要在config.properties添加与fofa banner对应关系即可使用
```

## 相关截图
* fofa search
<img width="1000" alt="image" src="https://github.com/user-attachments/assets/b2400ddb-53a4-44e0-ba31-a3be74c0e22d">

* fscan
<img width="1000" alt="image" src="https://github.com/user-attachments/assets/cf4c74d2-c533-403a-94a1-4424baf3c3a6">

* swagger scan
<img width="1000" alt="image" src="https://github.com/user-attachments/assets/c069b07a-b499-4b6c-90a3-63891e662c0c">

* 项目管理
<img width="1000" alt="image" src="https://github.com/user-attachments/assets/cd3416ed-73f7-47d4-95d7-386a3f745cbe">
