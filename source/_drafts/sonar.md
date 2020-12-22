---
layout: draft
title: sonar
date: 2020-12-22 19:36:34
tags:
---


SonarQube包含三个部分：

1. SonarQube Server

在sonarQube server运行有以下三个进程：

Web Server: User Interface，用户可以访问的UI界面

Search Server: 基于Elasticsearch

Compute Engine: 负责处理代码分析报告，并把报告保存到SonarQube database中


2. Database Server

保存在代码扫描中的代码质量和安全问题。
SonarQube的配置


2. Scanner

build或者CI server



分析源代码

  Sonar scanner:
  
  Gradle

  官网移步[SonarScanner for Gradle](https://docs.sonarqube.org/latest/analysis/scan/sonarscanner-for-gradle/)
  
  通过gradle task在执行sonar分析。

  gradle的sonarQube插件


    anything else (CLI) 
    
    当构建工具没有scanner的时候，可以使用[SonarScanner](https://docs.sonarqube.org/latest/analysis/scan/sonarscanner/)

    



  Jenkins



  

  Maven
  .NET
  Azure DevOps
  Ant

对语言
  对所有支持的语言都可以进行静态分析源代码 .java
  对部分语言可以静态分析编译后的代码 .class


















installing and configuring a SonarQube scanner. 

The scanner can either run on your build or as part of your continuous integration (CI) pipeline performing a scan whenever your build process is triggered.


Anlayzing branches


Analyzing pull request

SonarLint:
一个IDE级别的插件，能够在本地给出分析结果。



