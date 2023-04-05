- [IM-Bloommaker](#im-bloommaker)
  - [1. Hello world](#1-hello-world)
  - [2. 创建Repository的词典项目和实体](#2-创建repository的词典项目和实体)
  - [3. 用户搜索事例](#3-用户搜索事例)
  - [4. 登记用户信息(上传文件控件和登记按钮)](#4-登记用户信息上传文件控件和登记按钮)
  - [5. 自定义脚本四则运算](#5-自定义脚本四则运算)
  - [6. 自定义脚本获取当前日期](#6-自定义脚本获取当前日期)
  - [7. 用户列表页面](#7-用户列表页面)
  - [8. 用户列表页面\_RichTable](#8-用户列表页面_richtable)
  - [9. 用户编辑页面](#9-用户编辑页面)
  - [10. 用户编辑页面\_RichTable](#10-用户编辑页面_richtable)
  - [11. 用户信息编辑处理](#11-用户信息编辑处理)
  - [12. 制作图表页面](#12-制作图表页面)

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

1. BloomMaker内容一栏表下新建内容![新建内容](screenshot/20230405110233.png)
2. 设计编辑 -> 放入标题级别1 -> 设置textContent固定值为"自定义脚本练习2" -> 放入表单容器 -> 设置textContent为变量操作(日期) -> rowCount为2 -> heading元素的textContent固定值为"获取日期" -> 第二个heading为"正则表达式" -> 放入两个输入文本到表格右侧![设计页面](screenshot/20230405110757.png)
3. 设置变量 如下四个变量![设置变量](screenshot/20230405110856.png)
4. 设置action"获取日期" 放入两个自定义脚本 输入Javascript获取当前年月日date方法 第二个自定义脚本中 使用正则表达式转换date方法获取的日期 然后格式化返回值给先前设置的变量today![设置action](screenshot/20230405111312.png)
5. 设置输入框value![设置value](screenshot/20230405111532.png)
6. 下方输入框value设置为today![设置value](screenshot/20230405111645.png)
7. 设置读取页面时![读取页面时](screenshot/20230405111800.png)
8. 保存 显示预览![预览](screenshot/20230405112026.png)
9. 新建路由![新建路由](screenshot/20230405112059.png)
10. 为认证用户设置权限

## 7. 用户列表页面

用户信息一览表页面用来显示在前面[登记用户信息](#4-登记用户信息上传文件控件和登记按钮)已登记的用户信息  
先从表中获取登记信息 再制作用户信息一览表  

1. 网站地图 -> LogicDesigner -> 流程定义一览 -> 新建
2. 输入输出设置 ![输入输出设置](screenshot/20230405113550.png)
3. 添加用户定义![添加用户定义](screenshot/20230405113738.png)
4. 用户定义ID: user_list 用户定义名: 获取用户列表
5. 用户类别检索 选中 "tutorial"ID "培训"类别名
6. SQL定义 -> 取得数据定义 ![SQL定义](screenshot/20230405114017.png)
7. 值被自动显示到返回值栏中 ![自动返回值栏中](screenshot/20230405114133.png)
8. 连接元素 ![连接元素](screenshot/20230405114309.png)
9. 双击结束元素 映射设置![映射设置](screenshot/20230405114426.png)
10. 新保存![新保存](screenshot/20230405114504.png)
11. 网站地图 -> LogicDesigner -> 路由表定义一览![路由表定义](screenshot/20230405114629.png)
12. 设置认证用户许可
13. BloomMaker内容一栏表下 -> 登记页面 设计编辑
14. 新建 列表页面 设置为main页面 ![新建页面](screenshot/20230405124147.png)
15. 设置变量 ![设置变量](screenshot/20230405124509.png)
16. 设置常量![设置常量](screenshot/20230405124641.png)
17. 多语言设置 list, edit, title2
18. 列表页面放入 标题级别1 textContent设置多语言list![标题](screenshot/20230405125020.png)
19. 设置工具栏列表item![工具栏列表item](screenshot/20230405125140.png)
20. 放入表单容器 将除标题级别2以外元素删除 设置其textContent变量值为多语言的list
21. 重复(imui)下 纵向表格 放入表单容器内 设置list元素为"userList" ![设置纵向表格](screenshot/20230405125438.png)
22. 设置第一个heading textContent变量值为多语言![设置第一个heading](screenshot/20230405125644.png)
23. 设置第二, 三个heading textContent变量值为多语言 ![设置第二, 三个heading](screenshot/20230405125811.png)
24. userList[0] -> userList[index] ![设置标签](screenshot/20230405130036.png) ![设置标签2](screenshot/20230405130141.png)
25. 设置一个图标![设置一个图标](screenshot/20230405130243.png)
26. 设置action ![设置action](screenshot/20230405130355.png)
27. ![读取页面时](screenshot/20230405130443.png)
28. 刷新图标![刷新图标](screenshot/20230405130529.png)
29. 保存 预览 ![预览](screenshot/20230405130651.png)

## 8. 用户列表页面_RichTable

1. BloomMaker内容一栏表下 -> 登记页面 设计编辑
2. 新建列表页面richtable -> 设置为main页面 ![列表页面richtable](screenshot/20230405130922.png)
3. 复制列表页面 标题级别1 和 表单容器 到 列表页面_RichTable -> 删除纵向表单(重复) -> 放入RichTable![放入RichTable](screenshot/20230405131155.png)
4. 新建变量 ![header](screenshot/20230405131416.png) ![index](screenshot/20230405131436.png)
5. header下创建下级变量 ![userCd](screenshot/20230405131523.png) ![userName](screenshot/20230405131550.png)
6. 设置元素![设置元素](screenshot/20230405131638.png)
7. 保存 预览![预览](screenshot/20230405131722.png)

## 9. 用户编辑页面

1. 网站地图 -> LogicDesigner -> 流程定义一览 -> 新建
2. 输入输出设置 ![输入输出设置](screenshot/20230405132018.png)
3. 用户定义SQL新建 ![用户定义sql](screenshot/20230405132104.png)  
4. 获取用户信息sql语句![获取用户信息sql语句](screenshot/20230405132204.png) 即在返回值栏中显示出 删除原有的输入值 新建一个![输入返回值](screenshot/20230405132500.png)
5. ![获取用户](screenshot/20230405135218.png)
6. 获取用户 映射设置![映射设置](screenshot/20230405135246.png)
7. 结束元素 映射设置![映射设置](screenshot/20230405135316.png)
8. 新保存 ![新保存](screenshot/20230405135346.png)
9. 设置路由 ![设置路由](screenshot/20230405135435.png)
10. 设置认证用户许可
11. BloomMaker内容一栏表下 -> 登记页面 设计编辑
12. 新建页面 命名为编辑页面 复制登记页面 标题级别1 和 表单容器 到 编辑页面 修改标题1 元素固有![修改标题1](screenshot/20230405135733.png)
13. 编辑按钮 ![编辑按钮](screenshot/20230405135817.png)
14. 删除搜索按钮
15. 新建变量 editUrl ![新建变量 editUrl](screenshot/20230405135943.png)
16. 新建responseData下变量 ![userEditResponse](screenshot/20230405140032.png)
17. 选择userEditResponse新建变量 ![user](screenshot/20230405140127.png)
18. 选择user新建变量 ![userCd](screenshot/20230405140159.png)
19. 同样方法新建两个userName 和 fileKey 变量
20. 设置常量 ![Id_get_user](screenshot/20230405140501.png)
21. 设置用户代码value![设置value](screenshot/20230405140736.png)![userCd](screenshot/20230405140603.png)
22. 设置用户名value ![userName](screenshot/20230405140816.png)
23. 设置文件上传value![fileKey](screenshot/20230405140842.png)
24. 创建一个从列表页面跳转到编辑页面的action
25. 执行自定义脚本 ![自定义脚本](screenshot/20230405141040.png)
26. 向URL发送请求 ![向URL发送请求](screenshot/20230405141127.png)
27. 打开页面设置为编辑页面 确认! ![打开页面](screenshot/20230405141140.png)
28. 返回列表action![返回列表action](screenshot/20230405141241.png)
29. 标题栏 中 设置showToolBar为选中状态 删除更新图标 ![删除更新图标](screenshot/20230405141422.png)
30. 点击返回图标 设置事件 ![返回图标 设置事件](screenshot/20230405141501.png)

## 10. 用户编辑页面_RichTable

1. BloomMaker内容一栏表下 -> 登记页面 设计编辑
2. 选择列表页面_RichTable 设为main页面
3. 新建action ![自定义脚本](screenshot/20230405142020.png)
4. 向URL发送请求 ![向URL发送请求](screenshot/20230405142105.png)
5. 设置打开页面 -> 决定 ![设置打开编辑页面](screenshot/20230405142131.png)
6. 选择RichTable属性下 ![RichTable属性下](screenshot/20230405142253.png)

## 11. 用户信息编辑处理

1. 网站地图 -> LogicDesigner -> 流程定义一览 -> 新建
2. 输入输出设置 ![输入](screenshot/20230405143049.png)
3. 常量设置 ![常量](screenshot/20230405143125.png)
4. SQL定义新建 ![SQL定义新建](screenshot/20230405143215.png) sql语句定义![sql语句定义](screenshot/20230405143244.png)
5. 删除createDate变量 ![删除createDate变量](screenshot/20230405143336.png)
6. 编辑流程![编辑流程](screenshot/20230405143610.png)
7. 编辑用户 映射设置 ![编辑用户 映射设置](screenshot/20230405143642.png)
8. 登记文件信息 映射设置 ![登记文件信息 映射设置](screenshot/20230405143710.png)
9. 分支条件设置 ![分支条件设置](screenshot/20230405143753.png) ![EL表达式](screenshot/20230405143818.png)
10. 新保存 ![新保存](screenshot/20230405143853.png)
11. 路由表定义一览 设置路由 ![设置路由](screenshot/20230405143927.png)
12. 认证用户权限设置
13. BloomMaker内容一栏表下 -> 登记页面 设计编辑
14. 变量requestData下新建变量 ![新建变量](screenshot/20230405144153.png)
15. 新建常量 ![新建常量](screenshot/20230405144230.png) ![新建常量](screenshot/20230405150222.png)
16. 新建action ![新建action](screenshot/20230405150645.png) 向uRL发送请求![uRL发送请求](screenshot/20230405150715.png) 显示信息![显示信息](screenshot/20230405150838.png)
17. 编辑按钮 事件下 点击时"编辑处理" ![编辑处理](screenshot/20230405150916.png)
18. 删除编辑按钮中disabled中的变量值
19. 保存

## 12. 制作图表页面

用来实时显示登记在这张表中的所有数据的情况  

1. 网站地图 -> LogicDesigner -> 流程定义一览 -> 新建
2. 输入输出设置 ![输入输出设置](screenshot/20230405152915.png)
3. 用户定义 SQL定义新建 ![SQL定义新建](screenshot/20230405154207.png) ![SQL定义](screenshot/20230405154225.png)
4. 输入值栏中变量删除 ![输入值栏中变量删除](screenshot/20230405154259.png)
5. ![连接流程](screenshot/20230405154320.png)
6. 打开 结束 映射设置 ![结束 映射设置](screenshot/20230405154356.png)
7. 新保存 ![新保存](screenshot/20230405154425.png)
8. 设置除饼图外其他图表 ![输入输出设置](screenshot/20230405154541.png)
9. 常量设置 ![常量设置](screenshot/20230405154609.png)
10. 用户定义 SQL定义新建 ![SQL定义新建](screenshot/20230405154644.png)
11. SQL定义 ![SQL定义](screenshot/20230405154702.png)
12. 输入值栏中变量删除 ![输入值栏中变量删除](screenshot/20230405154726.png)
13. 用户定义 -> JavaScript定义新建 ![JavaScript定义新建](screenshot/20230405154822.png)
14. 输入值返回值栏中变量设置![输入值返回值栏中变量设置](screenshot/20230405154900.png)
15. JavaScript定义 ![JavaScript定义](screenshot/20230405154952.png)
16. 连接流程![配置流程](screenshot/20230405155022.png)
17. 图标结果数组操作 映射设置 ![图标结果数组操作 映射设置](screenshot/20230405155115.png)
18. 结束 映射设置 ![结束 映射设置](screenshot/20230405155148.png)
19. 新保存 ![新保存](screenshot/20230405155225.png)
20. 登记其他图标路由 ![登记路由](screenshot/20230405155257.png)
21. 登记饼状图标路由 ![饼状图标路由](screenshot/20230405155329.png)
22. 设置认证用户许可
23. 新建 ![新建](screenshot/20230405155439.png) 
24. 设计编辑 放入标题级别1 textContent设置为 "图表显示"
25. 将图表下 饼图, 折线图, 柱状图, 雷达图放入右侧
26. 设置变量 ![设置变量](screenshot/20230405155819.png)
27. 设置常量 ![设置常量](screenshot/20230405155851.png) ![设置常量](screenshot/20230405155905.png)
28. 设置action ![发送请求](screenshot/20230405160048.png) ![发送请求](screenshot/20230405160159.png)
29. 容器设置 ![容器设置](screenshot/20230405160242.png)
30. 设置饼图属性 ![饼图属性](screenshot/20230405160401.png)
31. 设置折线图属性 ![折线图属性](screenshot/20230405160457.png) series选项中 ![series选项中](screenshot/20230405160539.png)
32. 设置柱状图属性 ![柱状图属性](screenshot/20230405160634.png) ![柱状图属性](screenshot/20230405160847.png) series选项同上
33. 设置雷达图属性 同上
34. 选中标题级别1 showToolbar选项打勾 删除更新图标
35. 返回图标修改为新建图标 ![返回图标修改为新建图标](screenshot/20230405161033.png)
36. 设置herf为登记页面的URL 点击新建图标后 就会跳转至登记页面 ![设置herf为登记页面的URL](screenshot/20230405161201.png)
37. 保存 -> 新建路由 ![新建路由](screenshot/20230405161255.png)
38. 设置认证用户许可
39. 设置门户 ![设置门户](screenshot/20230405161341.png)
40. 新建图标 ![新建](screenshot/20230405161447.png) ![新建](screenshot/20230405161523.png) ![新建](screenshot/20230405161544.png)
41. 设置权限 ![设置权限](screenshot/20230405161621.png)
42. 组门户管理菜单![组门户管理菜单](screenshot/20230405161639.png)
43. 门户组件添加![门户组件添加](screenshot/20230405161710.png) ![门户组件添加](screenshot/20230405161739.png)
44. 设置参照权限 ![设置权限](screenshot/20230405161800.png)
