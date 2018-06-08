# 数据库设计  [返回首页](./README.md)


## student 表（学生表）
|字段名|类型|长度|主键|是否为空|备注|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|id|int|11|主键|否|学生id|
|account|varchar|32||否|用户名|
|password|varchar|32||否|密码（md5加密）|
|name|varchar|10||否|名字|
|sex|tinyint|1||是|性别：1男2女3保密|
|student_num|varchar|15||否|学号|
|birthday|date|||是|出生年月|
|github_account|varchar|32||否|GitHub账号|
|create_time|datetime|||是|注册时间|
|update_time|datetime|||是|修改时间|


## teacher 表（教师表）
|字段名|类型|长度|主键|是否为空|备注|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|job_id|varchar|12|主键|否|教师工号|
|account|varchar|32||否|用户名|
|password|varchar|32||否|密码（md5加密）|
|name|varchar|10||否|名字|
|sex|tinyint|1||是|性别：1男2女3保密|
|birthday|date|||是|出生年月|
|github_account|varchar|32||否|GitHub账号|
|create_time|datetime|||是|注册时间|
|update_time|datetime|||是|修改时间|


## course 表（课程表）
|字段名|类型|长度|主键|是否为空|备注|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|course_id|varchar|12|主键|否|课程编号|
|course_name|varchar|32||否|课程名称|
|teacher_id|varchar|12|外键|否|教师工号|
|teacher_name|varchar|10||否|教师名称|
|position|varchar|32||否|上课地点|
|credit|tinyint|1||否|课程学分|
|period|tinyint|1||否|课程学时|
|term|varchar|32||否|开课学期|
|create_time|datetime|||是|创建时间|


## choice_course 表（选课表）
|字段名|类型|长度|主键|是否为空|备注|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|id|int|11|主键|否|选课id|
|course_id|varchar|12|外键|否|课程编号|
|stu_id|int|11|外键|否|学生id|
|teacher_id|varchar|12|外键|否|教师编号|
|create_time|datetime|||否|选课时间|


## project 表（实验表）
|字段名|类型|长度|主键|是否为空|备注|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|id|int|11|主键|否|实验id|
|stu_id|int|11|外键|否|学生id|
|project_id|tinyint|1|外键|否|实验id|
|project_name|varchar|32||否|实验名称|
|term|varchar|32||否|开课学期|
|weight|double|||否|实验权重|
|grade|double|||否|实验得分|
|description|varchar|255||是|实验描述|
|course_id|varchar|12|外键|否|课程id|
|teacher_id|varchar|12|外键|否|教师id|
|create_time|datetime|||否|添加时间|


## grade 表（评分项表）
|字段名|类型|长度|主键|是否为空|备注|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|id|int|11|主键|否|评分项id|
|stu_id|int|11|外键|否|学生id|
|project_id|tinyint|1|外键|否|实验id|
|teacher_id|varchar|12||否|教师id|
|scoring_item|varchar|32||否|评分项|
|sco_item_desc|varchar|255||是|描述|
|weight|double|||否|权重|
|remark|varchar|255||否|批改评价|
|grade|double|||是|得分|
|update_time|datetime|||否|批改时间|
