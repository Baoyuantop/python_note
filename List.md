
Python List 列表常见操作


1. 将L2中偶数放到L1


```python
L1 = [1,2,3,4,5]
L2 = [m  for m in L1 if m%2 ==0]
```

2. 将 L 增加三倍放到 L2


```python
L = [1,2,3,4,5]
L1 = L * 3
L2 = [m*3 for m in L]
print(L1)
print(L2)
```

    [1, 2, 3, 4, 5, 1, 2, 3, 4, 5, 1, 2, 3, 4, 5]
    [3, 6, 9, 12, 15]
    

非常灵活的操作方式，可以把每个数据做各种处理后放到新列表

长度函数： len( 字符串、数组、列表....)
区别与js .length( )方法 


```python
L = [1,2,3,'hello','world']
for m in L:
    print(m)
```

    1
    2
    3
    hello
    world
    

3. 多维列表枚举


```python
L = [[1,'one'],[2,'two'],[3,'three']]
for m,n in L:
    print(m,'  ',n)
```

    1    one
    2    two
    3    three
    

4. 查找列表特定元素


```python
L = [1,2,3,'hello','world']
m = 'hello'
if m in L:
    print('in L')
else:
    print( 'not in L')
```

    in L
    

列表操作方法
len,max,min,list

5. 帮助函数：  help(函数名)


```python
help(list)
```

    Help on class list in module builtins:
    
    class list(object)
     |  list(iterable=(), /)
     |  
     |  Built-in mutable sequence.
     |  
     |  If no argument is given, the constructor creates a new empty list.
     |  The argument must be an iterable if specified.
     |  
     |  Methods defined here:
     |  
     |  __add__(self, value, /)
     |      Return self+value.
     |  
     |  __contains__(self, key, /)
     |      Return key in self.
     |  
     |  __delitem__(self, key, /)
     |      Delete self[key].
     |  
     |  __eq__(self, value, /)
     |      Return self==value.
     |  
     |  __ge__(self, value, /)
     |      Return self>=value.
     |  
     |  __getattribute__(self, name, /)
     |      Return getattr(self, name).
     |  
     |  __getitem__(...)
     |      x.__getitem__(y) <==> x[y]
     |  
     |  __gt__(self, value, /)
     |      Return self>value.
     |  
     |  __iadd__(self, value, /)
     |      Implement self+=value.
     |  
     |  __imul__(self, value, /)
     |      Implement self*=value.
     |  
     |  __init__(self, /, *args, **kwargs)
     |      Initialize self.  See help(type(self)) for accurate signature.
     |  
     |  __iter__(self, /)
     |      Implement iter(self).
     |  
     |  __le__(self, value, /)
     |      Return self<=value.
     |  
     |  __len__(self, /)
     |      Return len(self).
     |  
     |  __lt__(self, value, /)
     |      Return self<value.
     |  
     |  __mul__(self, value, /)
     |      Return self*value.
     |  
     |  __ne__(self, value, /)
     |      Return self!=value.
     |  
     |  __repr__(self, /)
     |      Return repr(self).
     |  
     |  __reversed__(self, /)
     |      Return a reverse iterator over the list.
     |  
     |  __rmul__(self, value, /)
     |      Return value*self.
     |  
     |  __setitem__(self, key, value, /)
     |      Set self[key] to value.
     |  
     |  __sizeof__(self, /)
     |      Return the size of the list in memory, in bytes.
     |  
     |  append(self, object, /)
     |      Append object to the end of the list.
     |  
     |  clear(self, /)
     |      Remove all items from list.
     |  
     |  copy(self, /)
     |      Return a shallow copy of the list.
     |  
     |  count(self, value, /)
     |      Return number of occurrences of value.
     |  
     |  extend(self, iterable, /)
     |      Extend list by appending elements from the iterable.
     |  
     |  index(self, value, start=0, stop=9223372036854775807, /)
     |      Return first index of value.
     |      
     |      Raises ValueError if the value is not present.
     |  
     |  insert(self, index, object, /)
     |      Insert object before index.
     |  
     |  pop(self, index=-1, /)
     |      Remove and return item at index (default last).
     |      
     |      Raises IndexError if list is empty or index is out of range.
     |  
     |  remove(self, value, /)
     |      Remove first occurrence of value.
     |      
     |      Raises ValueError if the value is not present.
     |  
     |  reverse(self, /)
     |      Reverse *IN PLACE*.
     |  
     |  sort(self, /, *, key=None, reverse=False)
     |      Stable sort *IN PLACE*.
     |  
     |  ----------------------------------------------------------------------
     |  Static methods defined here:
     |  
     |  __new__(*args, **kwargs) from builtins.type
     |      Create and return a new object.  See help(type) for accurate signature.
     |  
     |  ----------------------------------------------------------------------
     |  Data and other attributes defined here:
     |  
     |  __hash__ = None
    
    

6. input接受内容全部为 str


```python
m = input('please input')
print(m)
```

    please input123456
    123456
    

List 增删改查

7. 在末尾插入值


```python
L = [1,2,3,4]
L.append(5)
L.append(6)
L.append([1,2,3,'hello'])
print(L)
```

    [1, 2, 3, 4, 5, 6, [1, 2, 3, 'hello']]
    

8. 任意位置插入，第一个参数位置，第二个参数为值


```python
L = [1,2,3,4]
L.insert(2,2)
L.insert(-1,-1)
print(L)
```

    [1, 2, 2, 3, -1, 4]
    

9. 直接按索引修改


```python
L = [1,2,3,4]
L[1] = 9
print(L)
```

    [1, 9, 3, 4]
    

10.del( )删除指定索引


```python
L = [1,2,3,4]
del(L[2])
print(L)
```

    [1, 2, 4]
    

11. remove( )删除指定值 配合查找


```python
L = [1,2,3,4]
L.remove(2)
print(L)
```

    [1, 3, 4]
    

12. 其他
倒置 reverse( )
排序 sort( )
删除末尾 pop( )


