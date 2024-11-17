# Basic Layout

[💻🌃代码地址](https://github.com/laohei7/ComposeDome/blob/main/app/src/main/java/com/laohei/composedemo/demo/BasicLayout.kt)

## Box

`Box` 将元素堆叠摆放，可以通过 `aligin()`、`contentAlignment` 指定元素摆放的位置。

<tabs>
    <tab title="默认">
        <code-block lang="kotlin">
            Box(
                modifier = Modifier.size(200.dp)
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text("从零开始的异世界生活")
            }
        </code-block>
        <img src="image.png" alt=""/>
    </tab>
    <tab title="contentAlignment">
        <code-block lang="kotlin">
            Box(
                modifier = Modifier.size(200.dp),
                contentAlignment = Alignment.Center
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text("从零开始的异世界生活")
            }
        </code-block>
        <img src="image_2.png" alt=""/>
    </tab>
    <tab title="align()">
        <code-block lang="kotlin">
            Box(
                modifier = Modifier.size(200.dp),
                contentAlignment = Alignment.Center
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text(
                    "从零开始的异世界生活",
                    modifier = Modifier.align(Alignment.BottomEnd)
                )
            }
        </code-block>
        <img src="image_3.png" alt=""/>
    </tab>
</tabs>

## Column

`Column` 将元素纵向垂直摆放。

- `horizontalAlignment`： 水平摆放方式
- `verticalArrangement`： 垂直摆放方式

<tabs>
    <tab title="默认">
        <code-block lang="Kotlin">
            Column(
                modifier = Modifier.size(200.dp),
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text(
                    "从零开始的异世界生活",
                )
                Icon(
                    imageVector = Icons.Default.Home,
                    contentDescription = ""
                )
            }
        </code-block>
        <img src="image_4.png" alt=""/>
    </tab>
    <tab title="（水平）Alignment.CenterHorizontally">
        <code-block lang="Kotlin">
            Column(
                modifier = Modifier.size(200.dp),
                horizontalAlignment = Alignment.CenterHorizontally,
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text(
                    "从零开始的异世界生活",
                )
                Icon(
                    imageVector = Icons.Default.Home,
                    contentDescription = ""
                )
            }
        </code-block>
        <img src="image_5.png" alt=""/>
    </tab>
    <tab title="（垂直）Arrangement.Center">
        <code-block lang="Kotlin">
            Column(
                modifier = Modifier.size(200.dp),
                horizontalAlignment = Alignment.CenterHorizontally,
                verticalArrangement = Arrangement.Center
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text(
                    "从零开始的异世界生活",
                )
                Icon(
                    imageVector = Icons.Default.Home,
                    contentDescription = ""
                )
            }
        </code-block>
        <img src="image_6.png" alt=""/>
    </tab>
    <tab title="（垂直）Arrangement.SpaceEvenly">
        <code-block lang="Kotlin">
            Column(
                modifier = Modifier
                    .width(200.dp)
                    .height(400.dp),
                horizontalAlignment = Alignment.CenterHorizontally,
                verticalArrangement = Arrangement.SpaceEvenly
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text(
                    "从零开始的异世界生活",
                )
                Icon(
                    imageVector = Icons.Default.Home,
                    contentDescription = ""
                )
            }
        </code-block>
        <img src="image_7.png" alt=""/>
    </tab>
    <tab title="（垂直）Arrangement.SpaceAround">
        <code-block lang="Kotlin">
            Column(
                modifier = Modifier
                    .width(200.dp)
                    .height(400.dp),
                horizontalAlignment = Alignment.CenterHorizontally,
                verticalArrangement = Arrangement.SpaceAround
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text(
                    "从零开始的异世界生活",
                )
                Icon(
                    imageVector = Icons.Default.Home,
                    contentDescription = ""
                )
            }
        </code-block>
        <img src="image_8.png" alt=""/>
    </tab>
    <tab title="（垂直）Arrangement.SpaceBetween">
        <code-block lang="Kotlin">
            Column(
                modifier = Modifier
                    .width(200.dp)
                    .height(400.dp),
                horizontalAlignment = Alignment.CenterHorizontally,
                verticalArrangement = Arrangement.SpaceBetween
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text(
                    "从零开始的异世界生活",
                )
                Icon(
                    imageVector = Icons.Default.Home,
                    contentDescription = ""
                )
            }
        </code-block>
        <img src="image_9.png" alt=""/>
    </tab>
    <tab title="（垂直）Arrangement.spacedBy()">
        <code-block lang="Kotlin">
            Column(
                modifier = Modifier
                    .width(200.dp)
                    .height(400.dp),
                horizontalAlignment = Alignment.CenterHorizontally,
                verticalArrangement = Arrangement.spacedBy(20.dp)
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text(
                    "从零开始的异世界生活",
                )
                Icon(
                    imageVector = Icons.Default.Home,
                    contentDescription = ""
                )
            }
        </code-block>
        <img src="image_10.png" alt=""/>
    </tab>

</tabs>

## Row

`Row` 将元素横向水平直摆放。

- `verticalAlignment`: 垂直摆放方式
- `horizontalArrangement`: 水平摆放方式

<tabs>
    <tab title="默认">
        <code-block lang="Kotlin">
            Row(
                modifier = Modifier
                    .width(400.dp)
                    .height(200.dp),
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text(
                    "从零开始的异世界生活",
                )
                Icon(
                    imageVector = Icons.Default.Home,
                    contentDescription = ""
                )
            }
        </code-block>
        <img src="image_11.png" alt=""/>
    </tab>
    <tab title="Alignment.CenterVertically">
        <code-block lang="Kotlin">
            Row(
                modifier = Modifier
                    .width(400.dp)
                    .height(200.dp),
                verticalAlignment = Alignment.CenterVertically,
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text(
                    "从零开始的异世界生活",
                )
                Icon(
                    imageVector = Icons.Default.Home,
                    contentDescription = ""
                )
            }
        </code-block>
        <img src="image_12.png" alt=""/>
    </tab>
    <tab title="Arrangement.Center">
        <code-block lang="Kotlin">
            Row(
                modifier = Modifier
                    .width(400.dp)
                    .height(200.dp),
                verticalAlignment = Alignment.CenterVertically,
                horizontalArrangement = Arrangement.Center
            ) {
                Image(
                    painter = painterResource(R.drawable.rem_icon_3),
                    contentDescription = ""
                )
                Text(
                    "从零开始的异世界生活",
                )
                Icon(
                    imageVector = Icons.Default.Home,
                    contentDescription = ""
                )
            }
        </code-block>
        <img src="image_13.png" alt=""/>
    </tab>
    <tab title="其他">
        <code-block lang="plain text">
            参考 `Column`，效果一样，只是将纵向改为水平。
        </code-block>
    </tab>
</tabs>

## LazyRow

`LazyRow` 用于高效显示水平滚动列表的组件。

元素对齐方式同 `Row` 的 `verticalAlignment` 和 `horizontalArrangement` 一致。

* `items`：用于动态生成子项，可以传入一个 List 或指定项数。
* `item`：用于定义单个内容，适合在自定义内容生成时使用。

<tabs>
<tab title="item()">
    <code-block lang="Kotlin">
        LazyRow(
            modifier = Modifier
                .width(400.dp)
                .height(200.dp)
        ) {
            item {
                Text(text = "Rem")
            }
            // 动态生成子项使用 items 代替
            repeat(10) {
                item {
                    Image(
                        painter = painterResource(R.drawable.rem_icon_2),
                        contentDescription = ""
                    )
                }
            }
        }
    </code-block>
    <img src="img1.gif" alt=""/>
</tab>

<tab title="items()">
    <code-block lang="Kotlin">
        val list = remember {
            listOf(
                R.drawable.rem_icon_3,
                R.drawable.rem_icon_2,
                R.drawable.rem_icon,
                R.drawable.rem_icon_5,
                R.drawable.rem_icon_6
            )
        }
        LazyRow(
            modifier = Modifier
                .width(400.dp)
                .height(200.dp)
        ) {
            items(2) {
                Text(text = "Rem $it")
            }
            items(list) {
                Image(
                    painter = painterResource(it),
                    contentDescription = ""
                )
            }
        }
    </code-block>
    <img src="img2.gif" alt=""/>
</tab>

</tabs>

## LazyColumn

`LazyColumn` 用于高效显示垂直滚动列表的组件。

元素对齐方式同 `Column` 的 `verticalArrangement` 和 `horizontalAlignment` 一致。

**其他参考 `LazyRow`，使用方式一致。**

`LazyColumn` 和 `LazyRow` 可以使用 `stickyHeader` 固定标题项的滚动列表。

<tabs>
    <tab title="stickyHeader()">
        <code-block lang="Kotlin">
            val list = remember {
                listOf(
                    R.drawable.rem_icon_3,
                    R.drawable.rem_icon_2,
                    R.drawable.rem_icon,
                    R.drawable.rem_icon_5,
                    R.drawable.rem_icon_6
                )
            }
            LazyColumn(
                modifier = Modifier
                    .width(200.dp)
                    .height(400.dp)
            ) {
                stickyHeader {
                    Text(
                        text = "TEXT",
                        modifier = Modifier
                            .fillMaxWidth()
                            .background(Color.Gray)
                    )
                }
                items(10) {
                    Row(
                        modifier = Modifier
                            .fillMaxWidth()
                            .height(60.dp),
                        verticalAlignment = Alignment.CenterVertically,
                        horizontalArrangement = Arrangement.spacedBy(10.dp)
                    ) {
                        Icon(
                            imageVector = Icons.Default.CheckCircle,
                            contentDescription = ""
                        )
                        Text(text = "Item $it")
                    }
                }
                stickyHeader {
                    Text(
                        text = "IMAGE",
                        modifier = Modifier
                            .fillMaxWidth()
                            .background(Color.Gray)
                    )
                }
                items(list) {
                    Image(
                        painter = painterResource(it),
                        contentDescription = ""
                    )
                }
            }
        </code-block>
        <img src="img3.gif" alt=""/>
    </tab>
</tabs>

## FlowRow


`FlowRow` 是一种在 ltr 布局中从左到右（ltr）或在 rtl 布局中从右到左（rtl）填充项目的布局，当它用完空间时，
移动到位于底部的下一个“行”，然后继续填充项目直到项目用完。

```Kotlin
    FlowRow(
        modifier = Modifier.width(360.dp),
        verticalArrangement = Arrangement.spacedBy(20.dp),
        horizontalArrangement = Arrangement.SpaceAround
    ) {
        repeat(9) {
            Card {
                Text(text = "item $it")
                Image(
                    painter = painterResource(R.drawable.rem_icon),
                    contentDescription = "",
                    modifier = Modifier.size(100.dp)
                )
            }
        }
    }
```

![image_16.png](image_16.png)

## FlowColumn

同 `FlowRow`，仅在排列方式上由行改为列，使用方式基本一样。

![image_17.png](image_17.png)

## LazyVerticalGrid


<tabs>
    <tab title="Fixed()">
        定义具有固定行数或列数的网格。例如，对于垂直 Fixed(3） 意味着父组件宽度有 3 列，各占 1/3。
        <code-block lang="Kotlin">
            // ...
            LazyVerticalGrid(
                columns = GridCells.Fixed(5)
            ) {
                items(list) {
                    Surface(
                        color = Color(
                            red = Random.nextInt(255),
                            blue = Random.nextInt(255),
                            green = Random.nextInt(255),
                        )
                    ) {
                        Image(
                            painter = painterResource(it),
                            contentDescription = "",
                            modifier = Modifier.fillMaxSize()
                        )
                    }
                }
            }
        </code-block>
        <img src="image_18.png" alt=""/>
    </tab>
    <tab title="Adaptive()">
        定义具有尽可能多的行或列的网格，条件是每个单元格至少具有 minSize 空间并且所有额外空间均匀分布。
        例如，对于垂直 LazyVerticalGrid Adaptive（20.dp） 意味着将有尽可能多的列，每列至少为 20.dp，
        并且所有列的宽度都相等。如果屏幕宽度为 88.dp，则将有 4 列，每列 22.dp 。
        <code-block lang="Kotlin">
            // ....
            LazyVerticalGrid(
                columns = GridCells.Adaptive(60.dp)
            ) {
                items(list) {
                    Surface(
                        color = Color(
                            red = Random.nextInt(255),
                            blue = Random.nextInt(255),
                            green = Random.nextInt(255),
                        )
                    ) {
                        Image(
                            painter = painterResource(it),
                            contentDescription = "",
                            modifier = Modifier.fillMaxSize()
                        )
                    }
                }
            }
        </code-block>
        <img src="image_19.png" alt=""/>
    </tab>
    <tab title="FixedSize()">
            定义具有尽可能多的行或列的网格，条件是每个单元格都正好占用大小空间。剩余空间将通过 LazyGrid 安排在相应的轴上。
            如果 size 大于容器大小，则单元格的大小将与容器匹配。例如，对于垂直 LazyGrid FixedSize（20.dp） 意味着将有尽
            可能多的列，并且每列都将正好为 20.dp。如果屏幕宽度为 88.dp，则将有 4 列 20.dp，其余 8.dp 
            通过 Arrangement.Horizontal。
            <code-block lang="Kotlin">
                // ....
                LazyVerticalGrid(
                    columns = GridCells.FixedSize(60.dp)
                ) {
                    items(list) {
                        Surface(
                            color = Color(
                                red = Random.nextInt(255),
                                blue = Random.nextInt(255),
                                green = Random.nextInt(255),
                            )
                        ) {
                            Image(
                                painter = painterResource(it),
                                contentDescription = "",
                                modifier = Modifier.fillMaxSize()
                            )
                        }
                    }
                }
            </code-block>
            <img src="image_20.png" alt=""/>
        </tab>
</tabs>


## LazyHorizontalGrid

同 `LazyVerticalGrid`，仅排列方式上由列改为行。

![img4.gif](img4.gif)

## LazyVerticalStaggeredGrid

```Kotlin
    LazyVerticalStaggeredGrid(
        columns = StaggeredGridCells.Fixed(2)
    ) {
        items(list) {
            Surface(
                color = Color(
                    red = Random.nextInt(255),
                    blue = Random.nextInt(255),
                    green = Random.nextInt(255),
                )
            ) {
                Image(
                    painter = painterResource(it),
                    contentDescription = "",
                    modifier = Modifier.fillMaxSize()
                )
            }
        }
    }
```

![image_21.png](image_21.png)

## LazyHorizontalStaggeredGrid

同 `LazyVerticalStaggeredGrid`，使用方式基本一样。

![img5.gif](img5.gif)

## HorizontalPager

```Kotlin
    val list = remember {
        listOf(
            R.drawable.rem_icon_3,
            R.drawable.rem_icon_2,
            R.drawable.rem_icon,
            R.drawable.rem_icon_5,
        )
    }

    val pagerState = rememberPagerState { list.size }

    HorizontalPager(
        state = pagerState
    ) {
        Image(
            painter = painterResource(list[it]),
            contentDescription = ""
        )
    }
```

![img6.gif](img6.gif)

## VerticalPager

同 `HorizontalPager`，使用方式基本一样。

![img7.gif](img7.gif)