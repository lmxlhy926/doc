```shell
pwd     #当前目录路径
cd 		#家目录
cd -	#先前工作的目录
file filename 	#显示文件类型
less filename 	#浏览文件内容，只能浏览不能修改
```

#### ls

```shell
ls -a   #列出所有文件包括被隐藏的隐藏文件
ls -d	#显示目录信息而不是目录下文件的信息
ls -lh	#以字节数来显示文件大小
ls -t   #按修改时间来排序
```

#### cp

```shell
-u : 把文件从一个目录复制到另一个目录，仅复制目标目录不存在的或新于目标目录的文件
-r : 递归的复制目录及目录中的内容。复制目录时需要这个选项
	
cp file1 file2			#file2已存在则被重写，不存在则创建之
cp file1 file2 dir1		#复制file1,file2到dir1中，dir1必须存在
cp -r dir1 dir2			#dir2不存在则创建之，存在则复制dir1及其内容到dir2中
```

#### mv

```shell
移动后源文件不再存在
-u：把文件从一个目录移动到另一个目录，仅移动目标目录不存在的或新于目标目录的文件

mv file1 file2	 		#file2存在则内容被重写，不存在则创建file2
mv file1 file2 dir1		#移动file1,file2到目录dir1中。dir1必须存在
mv dir1 dir2			#dir2不存在则创建之，存在则移动dir1及其内容到dir2中
```

