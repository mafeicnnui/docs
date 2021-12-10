一、检测类函数



| 函数名                                     | 示例                  | 备注             |
| ------------------------------------------ | --------------------- | ---------------- |
| toTypeName                                 | SELECT toTypeName(0); | UInt8(三位数为8) |
| SELECT toTypeName(-0);                     | Int8                  |                  |
| SELECT toTypeName(-343);                   | Int16                 |                  |
| SELECT toTypeName(12.43);                  | Float64               |                  |
| SELECT toTypeName(toFloat32(12.43));       | Float32               |                  |
| SELECT toTypeName(12.34343);               | Float64               |                  |
| SELECT toTypeName(toDateTime(1502396027)); | DateTime              |                  |



二、数值型函数



| 函数名   | 示例                                      | 备注       |
| -------- | ----------------------------------------- | ---------- |
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



