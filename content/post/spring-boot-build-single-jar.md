---
title: "Spring Boot Build Single Jar报错：Compilation failure"
date: 2021-02-20T03:49:55+08:00
lastmod: 2021-02-20T03:49:55+08:00
draft: false
keywords: ["Spring", "Java", "Spring Boot"]
description: "[ERROR] No compiler is provided in this environment. Perhaps you are running on a JRE rather than a JDK?"
tags: ["Spring", "Java", "Spring Boot"]
categories: ["Java", "Error", "Exception", "Maven"]
author: ""

# You can also close(false) or open(true) something for this content.
# P.S. comment can only be closed
comment: false
toc: true
autoCollapseToc: true
postMetaInFooter: false
hiddenFromHomePage: false
# You can also define another contentCopyright. e.g. contentCopyright: "This is another copyright."
contentCopyright: false
reward: false
mathjax: false
mathjaxEnableSingleDollar: false
mathjaxEnableAutoNumber: false

# You unlisted posts you might want not want the header or footer to show
hideHeaderAndFooter: false

# You can enable or disable out-of-date content warning for individual post.
# Comment this out to use the global config.
#enableOutdatedInfoWarning: false

flowchartDiagrams:
  enable: false
  options: ""

sequenceDiagrams: 
  enable: false
  options: ""

---

<!--more-->
# 背景信息
此问题发生在阅读并且实践Spring Boot相关文档：https://spring.io/guides/gs/rest-service/的，想试下构建独立可运行的jar的时候。
> If you use Maven, you can run the application by using ./mvnw spring-boot:run. Alternatively, you can build the JAR file with ./mvnw clean package

```
➜  restful-web-service ./mvnw clean package
INFO] Scanning for projects...
[INFO]
[INFO] ------< cn.yzd3008.java.javaweb.spring.boot:restful-web-service >-------
[INFO] Building restful-web-service 0.0.1-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- maven-clean-plugin:3.1.0:clean (default-clean) @ restful-web-service ---
[INFO] Deleting /Users/yuduan/IdeaProjects/restful-web-service/target
[INFO]
[INFO] --- maven-resources-plugin:3.2.0:resources (default-resources) @ restful-web-service ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] Using 'UTF-8' encoding to copy filtered properties files.
[INFO] Copying 1 resource
[INFO] Copying 0 resource
[INFO]
[INFO] --- maven-compiler-plugin:3.8.1:compile (default-compile) @ restful-web-service ---
[INFO] Changes detected - recompiling the module!
[INFO] Compiling 3 source files to /Users/yuduan/IdeaProjects/restful-web-service/target/classes
[INFO] -------------------------------------------------------------
[ERROR] COMPILATION ERROR :
[INFO] -------------------------------------------------------------
[ERROR] No compiler is provided in this environment. Perhaps you are running on a JRE rather than a JDK?
[INFO] 1 error
[INFO] -------------------------------------------------------------
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  1.041 s
[INFO] Finished at: 2021-02-20T03:40:49+08:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-compiler-plugin:3.8.1:compile (default-compile) on project restful-web-service: Compilation failure
[ERROR] No compiler is provided in this environment. Perhaps you are running on a JRE rather than a JDK?
[ERROR]
[ERROR] -> [Help 1]
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException
➜  restful-web-service ./mvnw -e clean package
[INFO] Error stacktraces are turned on.
[INFO] Scanning for projects...
[INFO]
[INFO] ------< cn.yzd3008.java.javaweb.spring.boot:restful-web-service >-------
[INFO] Building restful-web-service 0.0.1-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- maven-clean-plugin:3.1.0:clean (default-clean) @ restful-web-service ---
[INFO] Deleting /Users/yuduan/IdeaProjects/restful-web-service/target
[INFO]
[INFO] --- maven-resources-plugin:3.2.0:resources (default-resources) @ restful-web-service ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] Using 'UTF-8' encoding to copy filtered properties files.
[INFO] Copying 1 resource
[INFO] Copying 0 resource
[INFO]
[INFO] --- maven-compiler-plugin:3.8.1:compile (default-compile) @ restful-web-service ---
[INFO] Changes detected - recompiling the module!
[INFO] Compiling 3 source files to /Users/yuduan/IdeaProjects/restful-web-service/target/classes
[INFO] -------------------------------------------------------------
[ERROR] COMPILATION ERROR :
[INFO] -------------------------------------------------------------
[ERROR] No compiler is provided in this environment. Perhaps you are running on a JRE rather than a JDK?
[INFO] 1 error
[INFO] -------------------------------------------------------------
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  0.887 s
[INFO] Finished at: 2021-02-20T03:41:59+08:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-compiler-plugin:3.8.1:compile (default-compile) on project restful-web-service: Compilation failure
[ERROR] No compiler is provided in this environment. Perhaps you are running on a JRE rather than a JDK?
[ERROR]
[ERROR] -> [Help 1]
org.apache.maven.lifecycle.LifecycleExecutionException: Failed to execute goal org.apache.maven.plugins:maven-compiler-plugin:3.8.1:compile (default-compile) on project restful-web-service: Compilation failure
No compiler is provided in this environment. Perhaps you are running on a JRE rather than a JDK?

    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:215)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:156)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:148)
    at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject (LifecycleModuleBuilder.java:117)
    at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject (LifecycleModuleBuilder.java:81)
    at org.apache.maven.lifecycle.internal.builder.singlethreaded.SingleThreadedBuilder.build (SingleThreadedBuilder.java:56)
    at org.apache.maven.lifecycle.internal.LifecycleStarter.execute (LifecycleStarter.java:128)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:305)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:192)
    at org.apache.maven.DefaultMaven.execute (DefaultMaven.java:105)
    at org.apache.maven.cli.MavenCli.execute (MavenCli.java:957)
    at org.apache.maven.cli.MavenCli.doMain (MavenCli.java:289)
    at org.apache.maven.cli.MavenCli.main (MavenCli.java:193)
    at sun.reflect.NativeMethodAccessorImpl.invoke0 (Native Method)
    at sun.reflect.NativeMethodAccessorImpl.invoke (NativeMethodAccessorImpl.java:62)
    at sun.reflect.DelegatingMethodAccessorImpl.invoke (DelegatingMethodAccessorImpl.java:43)
    at java.lang.reflect.Method.invoke (Method.java:498)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launchEnhanced (Launcher.java:282)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launch (Launcher.java:225)
    at org.codehaus.plexus.classworlds.launcher.Launcher.mainWithExitCode (Launcher.java:406)
    at org.codehaus.plexus.classworlds.launcher.Launcher.main (Launcher.java:347)
    at sun.reflect.NativeMethodAccessorImpl.invoke0 (Native Method)
    at sun.reflect.NativeMethodAccessorImpl.invoke (NativeMethodAccessorImpl.java:62)
    at sun.reflect.DelegatingMethodAccessorImpl.invoke (DelegatingMethodAccessorImpl.java:43)
    at java.lang.reflect.Method.invoke (Method.java:498)
    at org.apache.maven.wrapper.BootstrapMainStarter.start (BootstrapMainStarter.java:39)
    at org.apache.maven.wrapper.WrapperExecutor.execute (WrapperExecutor.java:122)
    at org.apache.maven.wrapper.MavenWrapperMain.main (MavenWrapperMain.java:61)
Caused by: org.apache.maven.plugin.compiler.CompilationFailureException: Compilation failure
No compiler is provided in this environment. Perhaps you are running on a JRE rather than a JDK?

    at org.apache.maven.plugin.compiler.AbstractCompilerMojo.execute (AbstractCompilerMojo.java:1220)
    at org.apache.maven.plugin.compiler.CompilerMojo.execute (CompilerMojo.java:187)
    at org.apache.maven.plugin.DefaultBuildPluginManager.executeMojo (DefaultBuildPluginManager.java:137)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:210)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:156)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:148)
    at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject (LifecycleModuleBuilder.java:117)
    at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject (LifecycleModuleBuilder.java:81)
    at org.apache.maven.lifecycle.internal.builder.singlethreaded.SingleThreadedBuilder.build (SingleThreadedBuilder.java:56)
    at org.apache.maven.lifecycle.internal.LifecycleStarter.execute (LifecycleStarter.java:128)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:305)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:192)
    at org.apache.maven.DefaultMaven.execute (DefaultMaven.java:105)
    at org.apache.maven.cli.MavenCli.execute (MavenCli.java:957)
    at org.apache.maven.cli.MavenCli.doMain (MavenCli.java:289)
    at org.apache.maven.cli.MavenCli.main (MavenCli.java:193)
    at sun.reflect.NativeMethodAccessorImpl.invoke0 (Native Method)
    at sun.reflect.NativeMethodAccessorImpl.invoke (NativeMethodAccessorImpl.java:62)
    at sun.reflect.DelegatingMethodAccessorImpl.invoke (DelegatingMethodAccessorImpl.java:43)
    at java.lang.reflect.Method.invoke (Method.java:498)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launchEnhanced (Launcher.java:282)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launch (Launcher.java:225)
    at org.codehaus.plexus.classworlds.launcher.Launcher.mainWithExitCode (Launcher.java:406)
    at org.codehaus.plexus.classworlds.launcher.Launcher.main (Launcher.java:347)
    at sun.reflect.NativeMethodAccessorImpl.invoke0 (Native Method)
    at sun.reflect.NativeMethodAccessorImpl.invoke (NativeMethodAccessorImpl.java:62)
    at sun.reflect.DelegatingMethodAccessorImpl.invoke (DelegatingMethodAccessorImpl.java:43)
    at java.lang.reflect.Method.invoke (Method.java:498)
    at org.apache.maven.wrapper.BootstrapMainStarter.start (BootstrapMainStarter.java:39)
    at org.apache.maven.wrapper.WrapperExecutor.execute (WrapperExecutor.java:122)
    at org.apache.maven.wrapper.MavenWrapperMain.main (MavenWrapperMain.java:61)
[ERROR]
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException
```

# 问题分析
首先看错误提示：
> [ERROR] No compiler is provided in this environment. Perhaps you are running on a JRE rather than a JDK?

## 第一步：看输出堆栈
往往堆栈包含了明确的错误信息。发现是插件的堆栈调用出问题，没啥有用的。为了试验下，我总不可能现在去研究插件的源码吧...
继续看到有个提示：http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException
去看了下，没啥有用的信息，先略过再说。

## 第二步，看错误信息
没找到complier？终端直接运行编译器：javac，
```
➜  ~ javac
用法: javac <options> <source files>
其中, 可能的选项包括:
  -g                         生成所有调试信息
  -g:none                    不生成任何调试信息
  -g:{lines,vars,source}     只生成某些调试信息
  -nowarn                    不生成任何警告
  -verbose                   输出有关编译器正在执行的操作的消息
  -deprecation               输出使用已过时的 API 的源位置
  -classpath <路径>            指定查找用户类文件和注释处理程序的位置
  -cp <路径>                   指定查找用户类文件和注释处理程序的位置
  -sourcepath <路径>           指定查找输入源文件的位置
  -bootclasspath <路径>        覆盖引导类文件的位置
  -extdirs <目录>              覆盖所安装扩展的位置
  -endorseddirs <目录>         覆盖签名的标准路径的位置
  -proc:{none,only}          控制是否执行注释处理和/或编译。
  -processor <class1>[,<class2>,<class3>...] 要运行的注释处理程序的名称; 绕过默认的搜索进程
  -processorpath <路径>        指定查找注释处理程序的位置
  -parameters                生成元数据以用于方法参数的反射
  -d <目录>                    指定放置生成的类文件的位置
  -s <目录>                    指定放置生成的源文件的位置
  -h <目录>                    指定放置生成的本机标头文件的位置
  -implicit:{none,class}     指定是否为隐式引用文件生成类文件
  -encoding <编码>             指定源文件使用的字符编码
  -source <发行版>              提供与指定发行版的源兼容性
  -target <发行版>              生成特定 VM 版本的类文件
  -profile <配置文件>            请确保使用的 API 在指定的配置文件中可用
  -version                   版本信息
  -help                      输出标准选项的提要
  -A关键字[=值]                  传递给注释处理程序的选项
  -X                         输出非标准选项的提要
  -J<标记>                     直接将 <标记> 传递给运行时系统
  -Werror                    出现警告时终止编译
  @<文件名>                     从文件读取选项和文件名
```
有javac啊！
## 第三步，检查javac
命令行运行及其结果，
```
➜  ~ which javac
/usr/bin/javac
➜  ~ ls -alh /usr/bin | grep java
-rwxr-xr-x     1 root   wheel   136K  1  1  2020 java
-rwxr-xr-x     1 root   wheel   136K  1  1  2020 javac
-rwxr-xr-x     1 root   wheel   136K  1  1  2020 javadoc
-rwxr-xr-x     1 root   wheel   136K  1  1  2020 javah
-rwxr-xr-x     1 root   wheel   136K  1  1  2020 javap
-rwxr-xr-x     1 root   wheel   136K  1  1  2020 javapackager
-rwxr-xr-x     1 root   wheel   136K  1  1  2020 javaws
```
But,我记得我的JDK是安装在：/Library/Java/JavaVirtualMachines/jdk1.8.0_271.jdk/Contents/Home
估计是mvnw犯傻了，不是使用的JDK下面的这个javac！
## 第四步：验证猜想
在.zshrc里面加入对应的JAVA_HOME，同时刷新当前SHELL环境变量，重新试下，
```
➜  ~ vi .zshrc # 编辑配置文件

104 # Java developer settings
105 export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_271.jdk/Contents/Home
106 export ANT_HOME=/Users/yuduan/Programmer/Java/bin/apache-ant-1.10.9
107 export M2_HOME=/Users/yuduan/Programmer/Java/bin/apache-maven-3.6.3
108 export CATALINA_HOME=/Users/yuduan/Programmer/Java/bin/apache-tomcat-9.0.41
109 export GRADLE_HOME=/Users/yuduan/Programmer/Java/bin/gradle-6.8

➜  restful-web-service source ~/.zshrc # 刷新SHELL
```
再次运行：./mvnw clean package，结果显示success！

# 写在最后
## 找RCA
最后查看项目文件源码：mvnw，发现有下面一段果然有问题：
```
if [ -z "$JAVA_HOME" ]; then
  javaExecutable="`which javac`"
  if [ -n "$javaExecutable" ] && ! [ "`expr \"$javaExecutable\" : '\([^ ]*\)'`" = "no" ]; then
    # readlink(1) is not available as standard on Solaris 10.
    readLink=`which readlink`
    if [ ! `expr "$readLink" : '\([^ ]*\)'` = "no" ]; then
      if $darwin ; then
        javaHome="`dirname \"$javaExecutable\"`" # **此处的结果是：/usr/bin**
        javaExecutable="`cd \"$javaHome\" && pwd -P`/javac"
      else
        javaExecutable="`readlink -f \"$javaExecutable\"`"
      fi
      javaHome="`dirname \"$javaExecutable\"`"
      javaHome=`expr "$javaHome" : '\(.*\)/bin'`
      JAVA_HOME="$javaHome"
      export JAVA_HOME
    fi
  fi
fi

...
# Compiling the Java class
("$JAVA_HOME/bin/javac" "$javaClass") # 到这里肯定有问题了：/usr/bin/bin/javac系统里面怎么可能会有这个文件？出错肯定就在所难免了
```
## 经验总结
遇事不慌，顺藤摸瓜，大胆猜想，小心求证！
