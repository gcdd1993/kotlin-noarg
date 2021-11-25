# Kotlin Noarg 使用

官方有文档介绍了[no-arg-plugin](https://kotlinlang.org/docs/no-arg-plugin.html)，但是只提供了Gradle插件，其中提到使用方法

```groovy
noArg {
    annotation("com.my.Annotation")
}
```

引入插件后，需要自定义一个注解，来识别哪些类需要进行无参构造器的添加。

看似很简单，也很灵活，但是实际上，每个项目都需要在项目内定义一个注解`com.xxx.NoArg`，然后配置

```groovy
noArg {
    annotation("com.xxx.NoArg")
}
```

有点傻不是吗？或许可以在公司内公共Maven仓库内定义一个Jar，里面放入`com.xxx.NoArg`，但实际上也有点多余。

所以本项目解决这个问题，让`no-arg-plugin`使用起来更加顺畅一点点

代码很简单，实际只有一行

```kotlin
annotation class NoArg
```

## 使用

```groovy

```



