title: Location
---

使用 `Location` 实例进行读写地理位置数据和查询。


## 方法

### initCustomPosition

##### 定义

`initCustomPosition(PositionOptions)`

##### 说明

初始化一个用户自定义的 Position 对象，可以自由设置 Position 中的属性。

##### 参数

| 参数名 | 说明 |
|---|---|
| PositionOptions | [PositionOptions](/location/Web/api/Location.html#PositionOptions) 类型，设置将要创建的本地媒体流属性。 |

##### 返回值

初始化成功的 `Position` 实例。

</br>

---

### set


##### 定义

`set(keyOrPositions[, position])`

##### 说明

手动将位置数据写入到对应节点。

##### 参数

| 参数名 | 说明 |
|---|---|
| keyOrPositions | String 或 Object 类型，如果类型为 String ，只有一个位置信息会保存，保存到这个 key 节点下。也可以是个包含 key 值和 [Position](Position.html) 对象的 Map ，一次写入多个位置。 |
| position | [Position](Position.html) 类型，当 keyOrPositions 为 String 时需要传这个 Position 参数。|

##### 返回值

Promise

</br>

---

### on


##### 定义

`on(key, callback)`

##### 说明

监听 key 对应的地理位置变化

##### 参数

| 参数名 | 说明 |
|---|---|
| key | String 类型，对应一个记录地理位置单位的唯一标识。 |
| callback | Function 类型，监听到 key 对应单位的地理位置发生变化时触发的回调。|

##### 返回值

[CallbackRegistration](CallbackRegistration.html)

</br>

---

### off


##### 定义

`off(key)`

##### 说明

取消所有监听key的位置信息。

##### 参数

| 参数名 | 说明 |
|---|---|
| key | String 类型，对应一个记录地理位置单位的唯一标识。 |

</br>

---

### once


##### 定义

`once(key)`

##### 说明

获取 key 当前的地理位置信息。

##### 参数

| 参数名 | 说明 |
|---|---|
| key | String 类型，对应一个记录地理位置单位的唯一标识。 |

##### 返回值

Promise<[Position](Position.html)>

</br>

---

### removePosition

##### 定义


`removePosition(key)`

##### 说明

删除 key 当前的地理位置信息。

##### 参数

| 参数名 | 说明 |
|---|---|
| key | String 类型，对应一个记录地理位置单位的唯一标识。 |

##### 返回值

Promise

</br>

---

### removePath

##### 定义


`removePath(key)`

##### 说明

删除 key 对应的轨迹信息。

##### 参数

| 参数名 | 说明 |
|---|---|
| key | String 类型，对应一条轨迹的唯一标识。 |

##### 返回值

Promise

</br>

---

### initCircleQuery

##### 定义


`initCircleQuery(circleQueryCriteria)`

##### 说明

用于查询某个范围内的点的类。

##### 参数

| 参数名 | 说明 |
|---|---|
| CircleQueryCriteria | [CircleQueryCriteria](Location.html#CircleQueryCriteria) 类型，范围查询的条件 Map。 |

##### 返回值

[CircleQuery](CircleQuery.html)

</br>

---

### initPathQuery


##### 定义

`initPathQuery(pathQueryCriteria)`

##### 说明

用于查询某个范围内的点的类。

##### 参数

| 参数名 | 说明 |
|---|---|
| PathQueryCriteria | [PathQueryCriteria](Location.html#PathQueryCriteria) 类型，范围查询的条件 Map。 |

##### 返回值

PathQuery

</br>

---

### initAMapLocationProviderWithTime


##### 定义

`initAMapLocationProviderWithTime(number)`

##### 说明

初始化一个根据时间间隔更新地理位置的 AMapLocationProvider 。

##### 参数

| 参数名 | 说明 |
|---|---|
| number | `Int` 类型，间隔时间，单位为 ms。 |

##### 返回值

[AMapLocationProvider](AMapLocationProvider.html)

</br>

---

### initAMapLocationProviderWithDistance


##### 定义

`initAMapLocationProviderWithDistance(number)`

##### 说明

初始化一个根据间隔距离更新地理位置的 AMapLocationProvider 。

##### 参数

| 参数名 | 说明 |
|---|---|
| number | `Float` 类型，间隔时间，单位为 m。 |

##### 返回值

[AMapLocationProvider](AMapLocationProvider.html)

</br>

---

### startTracing


##### 定义

`startTracing(key[, AMapLocationProvider])`

##### 说明

开启位置持续更新，用户可以传入 [AMapLocationProvider](AMapLocationProvider.html) 对象，默认以时间间隔为一秒的 [AMapLocationProvider](AMapLocationProvider.html) 进行更新。

##### 参数

| 参数名 | 说明 |
|---|---|
| key | `String` 类型，对应一个记录地理位置单位的唯一标识。 |
| AMapLocationProvider | [AMapLocationProvider](AMapLocationProvider.html) 类型，提供地理位置。 |

</br>

---

### stopTracing


##### 定义

`stopTracing(key)`

##### 说明

终止 key 的地理位置更新。

##### 参数

| 参数名 | 说明 |
|---|---|
| key | `String` 类型，对应一个记录地理位置单位的唯一标识。 |

</br>

---

### startRecordingPath


##### 定义

`startRecordingPath(key[, AMapLocationProvider])`

##### 说明

开启轨迹持续更新，用户可以传入 [AMapLocationProvider](AMapLocationProvider.html) 对象，默认以时间间隔为一秒的 [AMapLocationProvider](AMapLocationProvider.html) 进行更新。

##### 参数

| 参数名 | 说明 |
|---|---|
| key | `String` 类型，对应一个记录地理位置单位的唯一标识。 |
| AMapLocationProvider | [AMapLocationProvider](AMapLocationProvider.html) 类型，提供地理位置。 |

</br>

---

### stopRecordingPath


##### 定义

`stopRecordingPath(key)`

##### 说明

终止 key 的轨迹更新。

##### 参数

| 参数名 | 说明 |
|---|---|
| key | `String` 类型，对应一个轨迹的唯一标识。 |

</br>

---


### Location.distance


##### 定义

`Location.distance(position1, position2)`

##### 说明

计算两个点之间的距离, 单位 m。

##### 参数

| 参数名 | 说明 |
|---|---|
| Position | [Position](Position.html) 类型，一个地理位置对象。 |

##### 返回值

Number

</br>

---


## 常量

### PositionOptions

**类型**

```js
Object
```

##### 说明

设置将要创建的自定义位置对象的属性。

##### 参数

| 参数名 | 说明 |
|---|---|
| location | `Array` 类型。<br>一个包含经纬度的数组，数组的第一个数据为 float 型的纬度，第二个数据为 float 型的经度。|
| timestamp | `Int` 类型。<br>时间戳。 |
| customAttributes | `String` 类型。<br>用户自定义属性，如果是 Object 类型需转换成 String 后进行保存。 |

### CircleQueryCriteria

**类型**

```js
Object
```

##### 说明

设置范围查询的条件。

##### 参数

| 参数名 | 说明 |
|---|---|
| center | [Position](Position.html) 类型。<br>一个 Position 对象，将作为范围查询的中心。|
| radius | `Int` 类型。<br>范围查询的半径，单位是 m 。 |

### PathQueryCriteria

**类型**

```js
Object
```

##### 说明

设置轨迹查询的条件。

##### 参数

| 参数名 | 说明 |
|---|---|
| key | `String` 类型。<br>一个轨迹的唯一标识符。|
| startTime | `Int` 类型。<br>查询轨迹的开始时间，一个时间戳。 |
| endTime | `Int` 类型。<br>查询轨迹的结束时间，一个时间戳。 |
