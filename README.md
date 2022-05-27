# kr-jenkins-change-log

## 安装插件
```
系统管理 --> 插件管理 --> 高级 --> 本地安装 --> deploy
```

## 添加 change log 环境变量
```
+ 构建环境 --> Add Changelog Information to Environment
  + Entry Format --> %3$s(at %4$s via %1$s)\n
  + Date Format --> yyyy-MM-dd HH:mm:ss
+ 构建 --> 执行 shell
  + curl -H "Content-Type: application/json" -d "#~#${SCM_CHANGELOG}#~#" http://localhost:7777/hook/58b615db-01b5-4525-89e3-fb9472785db6
```
