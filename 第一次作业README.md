# 简单学生信息管理系统
本系统通过C++语言进行编写，具有增加，删减，查询，显示学生信息的相关功能，以实现简单的学生信息管理功能。
## 系统特色
- 具有登录功能，初始密码为12345。
- 录入信息十分全面，查询功能方便快捷。
## 运行前提
您的计算机需要提前装好C++的相关编译器。
## 部分代码
##### 主程序代码：
```C++
int main()
{
	int choice;
	entry();
loop://主菜单
	cout << "\t\t*******班级同学信息管理程序*******\n";
	cout << "\t\t* 1.加入同学信息                 *\n";
	cout << "\t\t* 2.删除同学信息                 *\n";
	cout << "\t\t* 3.显示同学信息                 *\n";
	cout << "\t\t* 4.查找信息                     *\n";
	cout << "\t\t* 5.退出程序                     *\n";
	cout << "\t\t**********************************\n";
	cout << "请选择功能：";
	cin >> choice;
	switch (choice)
	{
	case 1:
		add(stu);
		goto loop;
	case 2:
		deleted(stu);
		goto loop;
	case 3:
		cout << "\t\t1.显示本次运行程序录入的信息" << endl;
			display1(stu);
		goto loop;
	case 4:
		inquire(stu);
		goto loop;
	case 5:
		return 0;

	}
}

```
##### 查询功能代码:
```C++
void inquire(Student stu[])//查找功能
{
	int  i;
	char stuid[15], stuname[15];
		cout << "请输入学号：" << endl;
		cin >> stuid;
		for (i = 0;i < sum;i++)
		{
			if (strcmp(stu[i].id, stuid) == 0)
			{
				cout << "姓名\t" << "姓氏\t" << "学号\t" << "宿舍\t" << "QQ\t\t" << "手机号\t\t" << endl;
				cout << stu[i].name << "\t" << stu[i].lastname << "\t" << stu[i].id << "\t" <<
					stu[i].dorm << "\t" << stu[i].qq << "\t" << stu[i].phone << "\t" << endl;
			}
			else cout << "查无此人" << endl;
		}
}
```
<br/>

## 使用及测试结果
系统首先需要使用初始密码12345登录，然后可以选择加入，删除，显示，查找学生信息四个功能选项，也可以选择退出系统。

#### 测试结果：
##### 1.录入功能
![测试结果](https://github.com/wyc1234567/Seatwork/blob/master/%E6%B5%8B%E8%AF%95%E7%BB%93%E6%9E%9C1.png?raw=true)
##### 2.删除功能
![测试功能2](https://github.com/wyc1234567/Seatwork/blob/master/%E6%B5%8B%E8%AF%95%E7%BB%93%E6%9E%9C2.png?raw=true)
##### 3.查找功能
![测试功能3](https://github.com/wyc1234567/Seatwork/blob/master/%E6%B5%8B%E8%AF%95%E7%BB%93%E6%9E%9C%E4%B8%89.png?raw=true)
<br/>

## 作者
电气1702   
王胤丞   U201711693
## license
Copyright (c) Microsoft Corporation. All rights reserved.