# NumericStrings

## 题解
通过动态规划拆解子问题. `A[.B][e|EC] | [.B][e|EC]`, 会有A,B,C三个子问题
动态转移方程没写好

## LeetCode题解
本题使用有限状态自动机。根据字符类型和合法数值的特点，先定义状态，再画出状态转移图，最后编写代码即可。

### 字符类型：

空格 「 」、数字「 0—90—9 」 、正负号 「 +-+− 」 、小数点 「 .. 」 、幂符号 「 eEeE 」 。

### 状态定义：

按照字符串从左到右的顺序，定义以下 9 种状态。

0. 开始的空格
1. 幂符号前的正负号
2. 小数点前的数字
3. 小数点、小数点后的数字
4. 当小数点前为空格时，小数点、小数点后的数字
5. 幂符号
6. 幂符号后的正负号
7. 幂符号后的数字
8. 结尾的空格

### 结束状态：

合法的结束状态有 2, 3, 7, 8 。

![图片](../assets/NumericStrings.png)
