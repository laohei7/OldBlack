# Modifier

[💻🌃代码地址](https://github.com/laohei7/ComposeDome/blob/main/app/src/main/java/com/laohei/composedemo/demo/ModifierDome.kt)


## 组件尺寸

<tabs>
    <tab title="size()">
        <code-block lang="Kotlin">
            Box(
                modifier = Modifier
                    .size(80.dp)
                    .background(Color.Red)
            ) {
                Text(text = "size(60.dp)")
            }
        </code-block>
    </tab>
    <tab title="width()、height()">
        <code-block lang="Kotlin">
            Box(
                modifier = Modifier
                    .width(120.dp)
                    .height(30.dp)
                    .background(Color.Green)
            ) {
                Text(text = "width(120.dp) and height(30.dp)")
            }
        </code-block>
    </tab>
    <tab title="fillMaxWidth()、fillMaxHeight()">
        <code-block lang="Kotlin">
            Box(
                modifier = Modifier
                    .fillMaxWidth()
                    .height(30.dp)
                    .background(Color.Yellow)
            ) {
                Text(text = "fillMaxWidth() and height(30.dp)")
            }
        </code-block>
    </tab>
    <tab title="fillMaxSize()">
        <code-block lang="Kotlin">
            Box(
                modifier = Modifier
                    .width(120.dp)
                    .height(120.dp)
                    .background(Color.Magenta),
                contentAlignment = Alignment.Center
            ) {
                Icon(
                    imageVector = Icons.Default.CheckCircle,
                    contentDescription = "",
                    modifier = Modifier.fillMaxSize()
                )
                Text(text = "icon fillMaxSize()", color = Color.Yellow)
            }
        </code-block>
    </tab>
</tabs>

<img src="image_14.png" alt=""/>

## 背景色

`background()` 设置背景色。

```kotlin
Modifier.background(Color.Red)
```

## 形状

`clip()` 设置组件形状： 圆形、圆角矩形等。

```Kotlin
val list = remember {
        listOf(
            CircleShape,
            RoundedCornerShape(20.dp),
            RoundedCornerShape(topStart = 20.dp, bottomEnd = 20.dp),
            RoundedCornerShape(topStart = 80.dp, bottomEnd = 20.dp),
            CutCornerShape(20.dp),
            AbsoluteCutCornerShape(topLeft = 80.dp, topRight = 80.dp),
            AbsoluteCutCornerShape(topLeft = 40.dp, topRight = 40.dp),
            AbsoluteCutCornerShape(topLeft = 80.dp, topRight = 0.dp),
        )
    }

    FlowRow(
        modifier = Modifier
            .fillMaxWidth()
            .padding(vertical = 10.dp, horizontal = 2.dp),
        horizontalArrangement = Arrangement.spacedBy(20.dp),
        verticalArrangement = Arrangement.spacedBy(20.dp)
    ) {
        list.forEach {
            Box(
                modifier = Modifier
                    .size(80.dp)
                    .clip(it)
                    .background(
                        Color(
                            red = Random.nextInt(255),
                            blue = Random.nextInt(255),
                            green = Random.nextInt(255),
                        )
                    )
            )
        }
    }
```

![image_15.png](image_15.png)

