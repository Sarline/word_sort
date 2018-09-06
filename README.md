# word_sort
将某文档中的每个单词都已字母顺序重排，并重新输出文档
# coding:utf-8
import json
# 导入json库，是为了最后出书单词的时候，以非列表的形式输出
def word_list():
# 读取本地文件，我这里的本地文件是单词库
	filename = 'M.txt'
	with open(filename) as list_py:
		contents = list_py.read()
		line = contents.split()
    # 将读取到的字符串进行切片操作
		for word in line:
			line_list = sorted(word)
      #将每一个单词都按照字母顺序重新排序
			line_end =  ''.join(line_list)
      # 将重排后的字母串按照非列表的形式输出
			# print line_end
			filename_02 = 'M_02.txt'
			with open(filename_02, 'a') as list_py:
				list_py.write(line_end + '\n')
        # 自动将排序好的字母写入一个新文件

word_list()
# 调用函数，执行以上操作
