## update 1.9.14.7 you should care

`compileOnly("com.tencent.tinker:tinker-android-anno:${TINKER_VERSION}")`
change
`compileOnly("com.tencent.tinker:tinker-android-anno-support:${TINKER_VERSION}")`

attention! don't not change `annotationProcessor("com.tencent.tinker:tinker-android-anno:${TINKER_VERSION}")`

some issue change annotationProcessor will compile error

## Getting started

```groovy
dependencies {
    api("com.tencent.tinker:tinker-android-lib:${TINKER_VERSION}")

    //optional, help to generate the final application
    annotationProcessor("com.tencent.tinker:tinker-android-anno:${TINKER_VERSION}")
    compileOnly("com.tencent.tinker:tinker-android-anno-support:${TINKER_VERSION}")
}

```

