﻿﻿
# 接口：getOneStudentInfo  [返回](../../README.md)
用例： [查看信息用例](../../md/查看用户信息.md)

- 功能：
    获取一个学生的所有信息。
    
- 权限：    
    老师和学生都可以调用这个API。
    
- API请求地址： 
    接口基本地址/v1/api/getOneStudentInfo/<user_id>/

- 请求方式 ：
    POST

- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |user_id|学生id|

    
- 返回实例：

        {         
            "status": true,
            "data":[
               "student_name":"梅恩",
               "student_id":201510414413,
               "class":"软工4班"
               "grade_avg":"平均实验成绩"
            ],
            "errors": ""
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |data|学生的个人信息|
  |errors|后台返回的提示信息|

