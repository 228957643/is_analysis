﻿
# 接口：login  [返回](../../README.md)
用例： [登录用例](../../md/登录.md)

- 功能：
    返回登录是否成功。
    
- 权限：    
    学生和老师都可以调用这个API
    
- API请求地址： 
    接口基本地址/v1/api/login

- 请求方式 ：
    POST

- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |account|账号|
  |password|密码|

    
- 返回实例：

        {         
            "status": true,
            "data": []
            "errors": "登录成功"
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |data|空|
  |errors|后台返回的提示信息|

