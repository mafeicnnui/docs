

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