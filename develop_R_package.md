# 开发R包的经验分享
首先需要安装一些必备的包,学习 Hadley Wickham 的 [R package ](http://r-pkgs.had.co.nz/r.html) 这本书
```r
install.packages('devtools')
## 检查R代码是否规范 
install.packages("formatR")
formatR::tidy_dir("R")
## 检查R包写的怎么样
install.packages("lintr")
lintr::lint_package()
```

## 用BiocManager来管理和安装github上面的包

BiocManager 负责解决biocondutor的依赖 然后还能调用devtools 和install.packages,这样写在R包里面的依赖包关系会被自动下载及更新。
```r
chooseCRANmirror()
install.packages("BiocManager")
BiocManager::install("jmzeng1314/humanid")
```

