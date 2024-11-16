# Basic Layout

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

## FlowColumn

## LazyVerticalGrid

## LazyHorizontalGrid

## LazyVerticalStaggeredGrid

## LazyHorizontalStaggeredGrid

