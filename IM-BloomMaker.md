- [IM-Bloommaker](#im-bloommaker)
  - [1. Hello world](#1-hello-world)
  - [2. 创建Repository的词典项目和实体](#2-创建repository的词典项目和实体)
  - [3. 用户搜索事例](#3-用户搜索事例)
  - [4. 登记用户信息(上传文件控件和登记按钮)](#4-登记用户信息上传文件控件和登记按钮)
  - [5. 自定义脚本四则运算](#5-自定义脚本四则运算)
  - [6. 自定义脚本获取当前日期](#6-自定义脚本获取当前日期)

# IM-Bloommaker  
  
---

## 1. Hello world

1. ![点击网站地图](screenshot/202304041908.png)  
2. ![点击内容一览表](screenshot/202304041910.png)  
3. 创建分类![新建分类](screenshot/202304041913.png)  
4. 输入内容名Hello World 点击登记![新建内容](screenshot/202304041916.png)  
5. 点击设计编辑 进入设计界面![设计布局](screenshot/202304041921.png)  
6. 新建名为nameValue变量值, 将其绑定到文本框的value设置为变量值, 修改按钮的value名为提交  
7. 新建一个节面 放入一个标题级别小窗口 放入标签 将标签元素固有设定为nameValue变量值![设置界面2](screenshot/202304041929.png)  
8. 设置action 在对话框中打开界面2![设置action](screenshot/202304041931.png)  
9. 设置关闭对话框action ![关闭最前面的对话框](screenshot/202304041932.png)  
10. 绑定action到按钮 ![绑定action](screenshot/202304041933.png)  ![设置第二个页面关闭action](screenshot/202304041934.png)
11. 点击预览, 并保存  
12. 点击路由定义一览表 并新建分类 设置分类ID,分类名![路由定义](screenshot/202304041935.png)  
13. 新建路由 设置路由ID, URL, 选择内容(创建好的Hello World) 路由名称中输入Hello World后点击登记按钮 路由创建完毕![创建路由](screenshot/202304041940.png)  
14. 设置权限 为认证用户设置权限![为认证用户设置权限](screenshot/202304041941.png)  

## 2. 创建Repository的词典项目和实体  

1. ![点击词典项目列表](screenshot/202304041956.png)  
2. 新增类别, 再选中状态下新建项目 勾选用途中的"数据和限制" 设置词典项目ID和名为: userID
3. 类型模板选择text 变量名设置都为userCd 在限制栏中选择字母和数字 点击添加限制: 仅小写字母 选择UserCd后点击添加限制  
4. 新建项目2 勾选用途中的"数据" 设置词典项目ID和名为: userName.
5. 数据的类型模板选择text 变量名设置都为userName
6. 点击影响范围确认按钮后 在注释栏中 输入"创建词典项目" 点击提交
7. 网站地图 Repository中实体一览列表 ![实体一览列表](screenshot/202304042007.png)
8. 新增类别, 再选中状态下新建实体 点击编辑实体项目 选中之前创建的userCd和userName 点击创建 影响范围确认的注释栏中输入"登记实体" 并保存
9. 词典项目成功登记到词典中  

## 3. 用户搜索事例

1. 在BloomMaker内容一览表中 新建内容 id 名为 user_edit 登记页面
2. 设计界面 输入实体选项中选择登记页面
3. 修改key1名为requestDate
4. 选择多语言 新建 ![新建 多语言](screenshot/202304042020.png) ![title](screenshot/202304042021.png) 用表格查看创建的多语言![用表格查看创建的多语言](screenshot/202304042023.png)
5. 放入标题级别1 选中标题 为其设置 多语言中的title
6. 布局中 放入"框" 在布局imui中选择横向表格 放入刚刚的"框" 修改固有元素为2
7. 放入表单控件中的 按钮, 放入两个输入文本到表格右侧
8. 设置元素名及变量![设置元素名和变量](screenshot/202304042029.png)
9. 设置action 显示点选用户搜索对话框 设置用户代码和用户名![设置action](screenshot/202304042030.png)
10. 点击"搜索用户" 设置事件![设置事件: 点击时](screenshot/202304042032.png)

## 4. 登记用户信息(上传文件控件和登记按钮)

1. 数据库操作菜单![数据库操作菜单](screenshot/202304042037.png)
2. SQL文件导入![SQL文件导入](screenshot/202304042038.png)
3. 使用IM-logicDesigner制作用户登记信息action然后转换成restAPI以url的形式提供给IM-BloomMaker的action来调用
4. 网站地图下流程定义一览 点击新建![流程定义一览](screenshot/202304042042.png)
5. 输入输出设置 登记用户没有返回值 所有没有输出![输入输出设置](screenshot/202304042044.png)
6. 设置常量![设置常量](screenshot/202304042046.png)
7. 打开sql定义编辑![sql定义新建](screenshot/202304042047.png)
8. ![用户类别编辑](screenshot/202304042048.png)
9. sql定义查询链接 设置查询类型为insert![sql定义查询](screenshot/202304042049.png)
10. ![等级用户元素](screenshot/202304042050.png)
11. ![IMbox元素](screenshot/202304042051.png)
12. ![等级文件信息](screenshot/20230404205245.png)
13. 连接起来![连接起来](screenshot/20230404205336.png)
14. 双击等级用户元素 一一映射 ![映射设置](screenshot/20230404205554.png)
15. 发布至directmessagebox设置映射 ![发布至directmessagebox设置映射](screenshot/20230404205815.png)
16. 设置分支元素 ![设置分支](screenshot/20230404205857.png) 当有文件上传时处理表达式![当有文件上传时处理表达式](screenshot/20230404205923.png)
17. 等级文件信息元素 ![等级文件信息映射](screenshot/20230404210025.png)
18. ![流程类别信息](screenshot/20230404210113.png)
19. 新保存![流程定义](screenshot/20230404210142.png)
20. 设置路由![设置路由](screenshot/20230404210326.png)
21. 许可设置
22. 进入BloomMaker一览表菜单
23. 设置filekey![设置filekey](screenshot/20230404210533.png)
24. 新建常量![新建Id_register](screenshot/20230404210625.png)![新建msg](screenshot/20230404210705.png)
25. 设置多语言![设置多语言](screenshot/20230404210816.png)
26. "搜索用户按钮"移动至框内![移动搜索按钮](screenshot/20230404210930.png)
27. 放入表单容器![表单容器](screenshot/20230404211014.png)
28. 把框放到表单标题下![把"框"放入表单](screenshot/20230404211136.png)表格rowCount修改为1
29. 设置多语言![设置多语言](screenshot/20230404211322.png)
30. 表单控制下文件上传放到文件信息表格内 设置textContent多语言![设置文件信息多语言](screenshot/20230404211525.png)
31. 设置action:登记处理![登记处理action](screenshot/20230404211648.png)
32. imui显示信息![显示信息](screenshot/20230404211824.png)
33. 设置点击登记按钮时 不为空![点击登记按钮时 不为空](screenshot/20230404211933.png)
34. 设置登记按钮action![设置登记按钮action](screenshot/20230404212025.png)
35. 设置文件上传的value![文件上传的value](screenshot/20230404212119.png)
36. 设置完成

## 5. 自定义脚本四则运算

1. BloomMaker内容一栏表下新建内容 ![新建内容](screenshot/20230404213915.png)
2. 放入标题级别1 命名为自定义脚本练习
3. 放入表单容器 删除除标题级别2以外内容 重命名为变量操作
4. 表单控件下输入数值 放入两个输入数值在表单标题下方 再放入一个下拉框再两个数值中间
5. 通用下放入标签在数值右侧 固定值修改为"="
6. 布局下 放入两个"框"在表单容器最下方
7. 表单控件下按钮放入第一个"框" value修改为"计算"
8. 输入数值放入第二个"框"
9. 页面设置如下![页面设置](screenshot/20230404214740.png)
10. 设置变量![设置变量](screenshot/20230404215058.png) ![设置变量](screenshot/20230404215139.png)
11. 设置四则运算action![四则运算action](screenshot/20230404215405.png)
12. 设置执行条件 ![执行条件](screenshot/20230404215634.png)
13. 设置"计算"按钮事件为"计算"
14. 保存 设置路由

## 6. 自定义脚本获取当前日期