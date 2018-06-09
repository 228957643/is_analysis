﻿
# 接口：getProjectScore  [返回](../../README.md)
用例： [评定成绩](../用例/评定成绩.md)

- 功能：
    返回一个实验的所有评分项。
    
- 权限：    
    老师：只有老师可以调用该API。
    
- API请求地址： 
    接口基本地址/v1/api/getProjectScore/<project_id>/

- 请求方式 ：
    GET

- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |project_id|实验编号|

    
- 返回实例：

        {         
            "status": true,
            "data": [
                {
                    "project_name":"实验一",
                    "project_id":22,
                    "grade":90,
                    "score":[
                        {
                            "score_id":22,
                            "score_name":"评分项一"
                            "desc":"思路要清晰",
                            "score_grade":90,
                            "score_comment":"评价"
                        },
                        {
                        }
                    ]
                },
                {
                
                }
            ],    
            "errors": ""
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |data|返回的结果示例|
  |errors|后台返回的提示信息|

