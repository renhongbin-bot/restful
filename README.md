### 大气接口

```restful```风格接口规范: 

1. **请求方式**

【GET】 /users # 查询用户信息列表

【GET】 /users/1001 # 查看某个用户信息

【POST】 /users # 新建用户信息

【PUT】 /users/1001 # 更新用户信息(全部字段)

【PATCH】 /users/1001 # 更新用户信息(部分字段)

【DELETE】 /users/1001 # 删除用户信息

2. **接口使用```名词```不使用动词**

   /users

3. **接口路径中资源为```复数``而非单数**

   /users

4. **接口有多个单词路径以```减号```分割**

   /role-users

5. **查询参数(参数采用```下划线```分割)**

​	/users/{user_id}?user_name=root&user_password=123456

 6. **提交表单**

    使用postman ```x-www-from-urlencoded``` 格式提交

7. **data数据**

```ts
data: {

code: 1(代表成功) | 2(代表失败) | 其它状态码

data: {} | []

msg: 'success' | 'fail' | 其它状态

...其它数据,如tatol[总记录数]等
}
```

8. **使用token(```JWT加密校验```)验证登录信息**,设置对应的headers
