# 1、python指定传入参数类型

```python
def send_request(request_data : Any,
                 headers: Optional[Dict[str, str]],
                 user_id: Optional[UserId] = None,
                 as_json: bool = True)->str:

```

* request_data可以是任何数据
* header的内容是一个可选的字符串字典
* UserId是可选的（默认为None），或者是符合编码UserId的任何数据
* as_json需要始终是一个布尔值（本质上是一个flag，即使名称可能没有提供这种提示）
* 返回值是str类型

# 2、for技巧

```python
pred_occupancy = [{"pred_occupancy": occ} for occ in pred[index:index + len(link_nodes)]]
```

可以写成下面的写法

```python
pred_occupancy = []
for i in range(index, index + len(link_nodes)):
    occupancy = pred[i]
    pred_dict = {"pred_occupancy": occupancy}
    pred_occupancy.append(pred_dict)

```

# 3、
