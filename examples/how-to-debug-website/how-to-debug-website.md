# 如何调试一个网站
- 公司内培

## 小型网站架构图
 ![](https://github.com/rainbow494/code-reference/blob/master/img/architectural.png)

## 子系统 / 运行环境 / 插件

- 子系统
	- 前台
	- 后台
	- 数据库
	- gps数据库
	- map数据库
	- ci

- 运行环境
	- chrome
	- .net
	- sql server
	- sql lite
	- nodejs

- 插件
	- kendoui
	- knockoutjs

## 调试工具 / 使用方法 / 文档？

- chrome
    - css  / html
        - less / source-map
            - [原理](http://www.ruanyifeng.com/blog/2013/01/javascript_source_map.html)

        - elementes
            - css (2 filters)
            - dom
            - responsive
            - event listner / dom break point

    
    - 持久化资源
        - resources

    - js 
        - source
            - pause on exception (first exception?)
            - black box
            - format
            - edit
            - mapping project???????

    - third part
        - kendoUI
        - knockoutJS
        
            
    - interface
        - console
            - log request
        - network
		    - bottle neck

	- others
        - profiler
        - console
            - time / timeEnd
        - timeLine
    

- .net
	- postman ?? demo
	- apiUtility64
	- vs
		- first throw exception
		- 多线程调试
	- windbug

- sql server
	- sql server profiler
	- sql management

- sql lite
	- [sqllite](http://www.oschina.net/news/43608/5-popular-and-free-sqlite-management-tools)

- nodejs
	- executor grunt
	- node-inspector

- kendoui
	- chrome-extension： kendo ui
- knockoutjs
	- chrome-extension： knockoutjs context debugger

## 问题定位
- 持久化数据
	- local storage
	- net work log / xml http request log
	- kendo UI extenstion
	- knoutoutjs extenstion
	- database

- 系统配置
	- sql lite
		```
		- dataSourceSpatial
		地图调试入口
		- special convert
		Con = new SQLiteConnection(@"URI=file:" + SpatialPath);
		- geo region connection
		```

	- gps 数据库mapping
		```
		acs.vehicle.name => gps.vehicle.id
		acs.vehicle.gpsid => gps.vehicle.ExternalID
		TFGPS.INI
		```

	- orm mapping
		> 2 PersistenceInfoProvider.cs files acs/extension


- 系统定位

- 美国测试环境
	- viewfinder buildagent

- 构建快速迭代环境 / 技巧
	- 前端环境

	- kendo UI 环境

	- webapi环境

	- 数据库环境

	- CI环境

	- 其它
		- regex
		- json

	- git
		- 回退代码

## 性能调试
	- 工具 / 技巧
    - chrome
	   - console.timer()
	      - chrome performance
	- .net 性能分析工具
	- 数据库性能分析工具

    - 已使用的性能优化技术
        - 延迟加载
            - kendogrid的virtual scroll
        - 缓存
            - LocalStorage
            - e-tag（未使用）
        - 传输
            - gzip压缩(20:1)
            - base64
        - 数据库
            - 临时表

    - 技术带来的问题
        - 延迟加载
            - kendogrid的virtual scroll， 代码复杂度的增加
        - 缓存问题
            - LocalStorage
            - 资源文件无法替换

## 数据迁移
	- 数据迁移的基本流程？
	- 数据的基本的导入导出

## 实例
