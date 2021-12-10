

### 一、检测类函数

| 函数名     | 示例                                       | 备注             |
| :--------- | ------------------------------------------ | :--------------- |
| toTypeName | SELECT toTypeName(0);                      | UInt8(三位数为8) |
|            | SELECT toTypeName(-0);                     | Int8             |
|            | SELECT toTypeName(-343);                   | Int16            |
|            | SELECT toTypeName(12.43);                  | Float64          |
|            | SELECT toTypeName(toFloat32(12.43));       | Float32          |
|            | SELECT toTypeName(12.34343);               | Float64          |
|            | SELECT toTypeName(toDateTime(1502396027)); | DateTime         |



### 二、数值型函数

| 函数名   | 示例                                      | 备注       |
| :------- | ----------------------------------------- | ---------- |
| plus     | SELECT plus(12, 21), plus(10, -10);       | 和         |
| Minus    | SELECT minus(10, 5), minus(10, -10);      | 差         |
| multiply | SELECT multiply(12, 2), multiply(12, -2); | 积         |
| divide   | SELECT divide(12, 4), divide(-4.5, 3);    | 除         |
| modulo   | SELECT modulo(10, 3),modulo(10.5, 3);     | 求余       |
| negate   | SELECT negate(10), negate(-10);           | 取反       |
| abs      | SELECT abs(-10), abs(10);                 | 绝对值     |
| gcd      | SELECT gcd(12, 24), gcd(-12, -24)         | 最大公约数 |
| lcm      | SELECT lcm(12, 24), lcm(-12, -24)         | 最小公倍数 |
|          |                                           |            |



### 三、比较函数

| 函数名            | 示例                                                   | 备注         |
| ----------------- | ------------------------------------------------------ | ------------ |
| ==、！=、<>       | SELECT 12 == 12, 12 != 10, 12 <> 12;                   | 相等、不相等 |
| Equals、notEquals | SELECT equals(12, 12), notEquals(12, 10);              | 相等、不相等 |
| greater           | SELECT greater(12, 10), greater(10, 12);               | 大于         |
| greaterOrEquals   | SELECT greaterOrEquals(12,10), greaterOrEquals(12,12); | 大于等于     |
| less              | SELECT less(12, 21), less(12, 10);                     | 小于         |
| lessOrEquals      | SELECT lessOrEquals(12, 120), lessOrEquals(12, 12);    | 小于等于     |

 说明：始终返回0表示false 或 1表示true



### 四、逻辑函数

| 函数名 | 示例                                                         | 备注 |
| ------ | ------------------------------------------------------------ | ---- |
| or     | SELECT 12==12 or 12!=10;SELECT or(equals(12, 12), notEquals(12, 10)); | 或   |
| and    | SELECT 12==12 and 12!=10;SELECT and(equals(12, 12), notEquals(12, 10)); | 与   |
| not    | SELECT not 12, not 0;SELECT not(12), not(0);                 | 非   |

说明：逻辑操作符（返回0表示false 或 1表示true）



### 五、转换函数

| 函数名    | 示例                                                | 备注             |
| --------- | --------------------------------------------------- | ---------------- |
| toInt8    | toInt8(12.3334343)                                  | 数值转8位整数    |
| toFloat32 | toFloat32(10.001)                                   | 数值转32位浮点数 |
| toFloat64 | toFloat64(1.000040)                                 | 数值转64位浮点数 |
|           | SELECT                                              |                  |
| cast      | '2016-06-15 23:00:00' AS timestamp,                 | 强制类型转换     |
|           | cast(timestamp AS DateTime) AS datetime,            |                  |
|           | cast(timestamp AS Date) AS date,                    |                  |
|           | cast(timestamp, 'String') AS string,                |                  |
|           | cast(timestamp, 'FixedString(22)') AS fixed_string; |                  |



| 函数名 | 示例                                    | 备注       |
| ------ | --------------------------------------- | ---------- |
| toDate | WITH                                    | 字符转日期 |
|        | toDate('2019-01-01') AS date,           |            |
|        | INTERVAL 1 WEEK AS interval_week,       |            |
|        | toIntervalWeek(1) AS interval_to_week,  |            |
|        | toIntervalMonth(1) AS interval_to_month |            |
|        | SELECT                                  |            |
|        | date + interval_week,                   |            |
|        | date + interval_to_week,                |            |
|        | date + interval_to_month;               |            |



| 函数名     | 示例                                           | 备注           |
| ---------- | ---------------------------------------------- | -------------- |
| toDateTime | WITH                                           | 字符转日期时间 |
|            | toDateTime('2019-01-01 12:10:10') as datetime, |                |
|            | INTERVAL 1 HOUR AS interval_hour,              |                |
|            | toIntervalHour(1) as invterval_to_hour         |                |
|            | SELECT                                         |                |
|            | plus(datetime, interval_hour),                 |                |
|            | plus(datetime, invterval_to_hour);             |                |
|            |                                                |                |
|            |                                                |                |



