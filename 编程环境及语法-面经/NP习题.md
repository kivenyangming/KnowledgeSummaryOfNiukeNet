
## 描述
牛牛、牛妹和牛可乐都是Nowcoder的用户，某天Nowcoder的管理员希望将他们的用户名以某种格式进行显示，\
现在给定他们三个当中的某一个名字name，请分别按全小写、全大写和首字母大写的方式对name进行格式化输出（注：每种格式独占一行）。\
输入描述：\
一行一个字符串表示名字。\
输出描述：\
请分别按全小写、全大写和首字母大写的方式对name进行格式化输出（注：每种格式独占一行）。
```
name=input()
print('%s'%name.lower(),
      '%s'%name.upper(),
      '%s'%name.title(),
      sep='\n')

name = input()
# 利用lower、upper、title方法将输入的name全转为 全小写、全大写、首字母大写
print(f'{name.lower()}')
print(f'{name.upper()}')
print(f'{name.title()}')
```

## 描述
牛牛、牛妹和牛可乐都是Nowcoder的用户，某天Nowcoder的管理员由于某种错误的操作导致他们的用户名的左右两边增加了一些多余的空白符（如空格或'\t'等），\
现在给定他们三个当中的某一个名字name，请输出name去掉两边的空白符后的原本的内容。\
输入描述：\
一行一个字符串表示名字name（注：name两边带有一些多余的空白符）。\
输出描述：\
一行输出name去掉两边的空白符后的原本的内容。
```
name = input()
print(name.strip())
```

使用print()语句直接打印字符串'PYTHON'.lower()和字符串'Python'.lower()是否相等的比较结果；
```
print('PYTHON'.lower() == 'python'.lower())
```

## 描述
牛牛正在练习心算能力，为了测试他算得准不准，他决定写一段简单的计算器小程序检验自己的心算能力。\
这个计算器要实现的功能包括：\
读入第一个数字记入变量x中，读入第二个数字记入变量y中；\
然后依次逐行用print函数打印x与y相加，x减去y，x与y相乘，x除以y（整除），x对y取余的计算结果。\
输入描述：\
输入两个整数，x与y，其中y不会为0\
输出描述：\
输出结果按照题目要求，每个计算结果单独一行。
```
x = int(input())
y = int(input())

print(x+y)
print(x-y)
print(x*y)
print(x//y)
print(x%y)
```

## 描述
为庆祝驼瑞驰在牛爱网找到合适的对象，所以驼瑞驰创建了一个依次包含字符串 'Niuniu' 和 'Niu Ke Le' 的列表guest_list，作为庆祝派对的邀请名单。\
请你依次对列表中的名字发送类似'Niuniu, do you want to come to my celebration party?'的句子。\
驼瑞驰的好朋友牛牛、GURR哥和LOLO姐也正好有空，所以请使用insert()方法把字符串'GURR'插入到列表guest_list的开头，\
再使用insert()方法把字符串'Niumei'插入到字符串'Niu Ke Le'的前面，再使用append()方法把字符串'LOLO'插入到列表guest_list的最后，\
再依次发送类似'Niuniu, thank you for coming to my celebration party!'的句子。\
输入描述：\
无\
输出描述：\
按题目描述进行输出即可（注意前后两个输出部分需以一个空行进行分隔）。\
Niuniu, do you want to come to my celebration party?\
Niu Ke Le, do you want to come to my celebration party?

GURR, thank you for coming to my celebration party!\
Niuniu, thank you for coming to my celebration party!\
Niumei, thank you for coming to my celebration party!\
Niu Ke Le, thank you for coming to my celebration party!\
LOLO, thank you for coming to my celebration party!
```
guest_list = ['Niuniu', 'Niu Ke Le']
for name in guest_list:
    print(name + ", do you want to come to my celebration party?")

guest_list.insert(0,'GURR')
guest_list.insert(2,'Niumei')
guest_list.append('LOLO')
print()
for name in guest_list:
    print(name + ", thank you for coming to my celebration party!")
```

## 描述
毕业季到了，牛牛为了找工作准备了自己简历，以及投递公司的列表company_list，其中包括了字符串 'Alibaba', 'Baidu', 'Tencent', 'MeiTuan', 'JD' 作为他投递简历的目标公司。\
请向列表中每个公司发送一条消息类似 'Hello Alibaba, here is my resume!'。\
然而，遗憾的是Alibaba、Tencent、MeiTuan、JD都没有通过牛牛的简历审核，只有Baidu回复了他，邀请他去参加面试。因此你需要：\
使用 del() 函数删除列表company_list中的字符串 'Alibaba'.\
使用 pop() 函数依次删除列表company_list中的字符串'JD'，'MeiTuan'.\
使用 remove() 函数删除列表company_list中的字符串'Tencent'.\
最后向列表中的剩余的公司发送类似 'Baidu, thank you for passing my resume. I will attend the interview on time!' 的消息
```
company_list = [ 'Alibaba', 'Baidu', 'Tencent', 'MeiTuan', 'JD' ]
for company in  company_list:
    print("Hello" + " " + company + ", here is my resume!")

del company_list[0]
company_list.pop(3)
company_list.pop(2)
company_list.remove('Tencent')
print()
print(company_list[0] + ", thank you for passing my resume. I will attend the interview on time!")
```

## 描述
创建一个依次包含字符串'P'、'y'、't'、'h'、'o'和'n'的列表my_list后，\
先使用print()语句一行打印字符串'Here is the original list:'，再直接使用print()语句把刚刚创建的列表my_list整个打印出来，

输出一个换行，再使用print()语句一行打印字符串'The result of a temporary reverse order:'，\
再使用print()语句把使用sorted()函数对列表my_list进行临时降序排序的结果整个打印出来；

输出一个换行，再使用print()语句一行打印字符串'Here is the original list again:'，\
再使用print()语句把原来的列表my_list整个打印出来，确认没有改变原来的列表my_list；

对列表my_list调用sort()方法，使列表my_list中的字符串以降序排序，\
输出一个换行，再使用print()语句一行打印字符串'The list was changed to:'，\
再使用print()语句把修改后的列表my_list整个打印出来，确认列表my_list的字符串以降序排序；

对列表my_list调用reverse()方法，使列表my_list中的字符串的位置前后翻转，\
输出一个换行，再使用print()语句一行打印字符串'The list was changed to:'，\
再使用print()语句把修改后的列表my_list整个打印出来，确认列表my_list的字符串的位置前后翻转了。
```
my_list = ['P','y','t','h','o','n']
print('Here is the original list:')
print(my_list)
print()

print('The result of a temporary reverse order:')
my_list0 = sorted(my_list,reverse = True)
print(my_list0)
print()

print('Here is the original list again:')
print(my_list)
print()

print('The list was changed to:')
my_list.sort(reverse = True)
print(my_list)
print()

print('The list was changed to:')
my_list.reverse()
print(my_list)
```

# 描述
创建一个依次包含字符串'Niuniu'、'Niumei'、'GURR'和'LOLO'的列表current_users，\
再创建一个依次包含字符串'GurR'、'Niu Ke Le'、'LoLo'和'Tuo Rui Chi'的列表new_users，\
使用for循环遍历new_users，如果遍历到的新用户名在current_users中，\
则使用print()语句一行输出类似字符串'The user name GurR has already been registered! Please change it and try again!'的语句，\
否则使用print()语句一行输出类似字符串'Congratulations, the user name Niu Ke Le is available!'的语句。（注：用户名的比较不区分大小写）
```
current_users = ['Niuniu','Niumei','GURR','LOLO']
new_users = ['GurR','Niu Ke Le','LoLo','Tuo Rui Chi']
for i in new_users:
    for y in current_users:
        if i.upper() == y.upper():
            print('The user name %s has already been registered! Please change it and try again!'%i)
            break
    else:
            print('Congratulations, the user name %s is available!'%i)
```

# 描述
创建一个依次包含键-值对'<': 'less than'和'==': 'equal'的字典operators_dict，\
先使用print()语句一行打印字符串'Here is the original dict:'，\
再使用for循环遍历 已使用sorted()函数按升序进行临时排序的包含字典operators_dict的所有键的列表，使用print()语句一行输出类似字符串'Operator < means less than.'的语句；

对字典operators_dict增加键-值对'>': 'greater than'后，\
输出一个换行，再使用print()语句一行打印字符串'The dict was changed to:'，\
再次使用for循环遍历 已使用sorted()函数按升序进行临时排序的包含字典operators_dict的所有键的列表，使用print()语句一行输出类似字符串'Operator < means less than.'的语句，确认字典operators_dict确实新增了一对键-值对。
```
operators_dict = {'<':'less than','==':'equal'}
print('Here is the original dict:')
for i, j in sorted(operators_dict.items()):
    print('Operator %s means %s.'%(i,j))
print("")

operators_dict['>']='greater than'
print('The dict was changed to:')
for i,j in sorted(operators_dict.items()):
    print('Operator %s means %s.'%(i,j))
```