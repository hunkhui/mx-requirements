# 保留率的展示方法

* 条件组合查询后，显示的结果，均是所有符合的**班级的列表**
* 结果列表中的每个班级的保留率，点击，可以进入该班级的学生列表，看去留情况
* 每次查询有一个`最终保留率`
  * `最终保留率` = `班级列表中，所有保留的学生总数` / `班级列表中的学生总数`
  * `最终保留率`单独显示在班级列表的右上方(Final Data)
* UI Demo

```
+----------------------------------------------------------------------------+
| +--------------+  +---------------+ +-------------+ +-------------+        |
| |campus        |  |course / Group | |teacher      | |class        |        |
| +--------------+  +---------------+ +-------------+ +-------------+        |
|                                                                            |
+----------------------------------------------------------------------------+
+----------------------------------------------------------------------------+
|                                                     +--------------------+ |
|                                                     | Final Data:        | |
|                                                     | 26 / 31 = 83.87%   | |
|                                                     +--------------------+ |
|                                                                            |
|                                                                            |
| +---------+---------------+------------------+--------------+------------+ |
| |class 1  |    16         |        16        |    0         |    100%    | |
| +---------+---------------+------------------+--------------+------------+ |
|                                                                            |
| +---------+---------------+------------------+--------------+------------+ |
| |class 2  |    15         |        10        |    5         |    66%     | |
| +---------+---------------+------------------+--------------+------------+ |

```
* 查询的条件
  * 校区(campus)
  * 课程(course) / 保留率奖金计算规则课程分组(group)
    * 课程，保留率奖金计算规则课程分组为单选
    * 详细内容，参考[保留率奖金计算规则课程分组](https://github.com/shchnmz/mx-requirements/blob/master/hr/pay/baoliulv-bonus/group-for-rules-of-baoliulv.md)
  * 教师(teacher)
  * 班级(class)
