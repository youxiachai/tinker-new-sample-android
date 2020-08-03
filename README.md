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

    //for 1.9.14.7 you must add it
    annotationProcessor("com.tencent.tinker:tinker-android-anno:${TINKER_VERSION}")
    compileOnly("com.tencent.tinker:tinker-android-anno-support:${TINKER_VERSION}")
}

```

## FAQ

### build: tinkerPatch throw
```
Caused by: com.tencent.tinker.android.dex.DexException: Unexpected magic: [100, 101, 120, 10, 48, 51, 56, 0]
```

check bakApk `*.apk` not from use AS `Run` button beacuase tinker not support `Apply Changes`

use `Make Project` and Manual install then run `tinkerPatch`

### error: cannot access Keep

```groovy
annotationProcessor("com.tencent.tinker:tinker-android-anno:${TINKER_VERSION}")
compileOnly("com.tencent.tinker:tinker-android-anno-support:${TINKER_VERSION}")
```

change 
```groovy
annotationProcessor("com.tencent.tinker:tinker-android-anno-support:${TINKER_VERSION}")
api("com.tencent.tinker:tinker-android-anno-support:${TINKER_VERSION}")
``
