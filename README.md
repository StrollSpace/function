# 说明
### 模仿jQuery的next(获取下一个弟弟)和nextAll(获取下面所有的弟弟)
  + next:获取指定元素下面的一个兄弟节点
  + nextAll：获取指定元素下面所有的兄弟节点
  + @parameter：
  	* ele：当前元素id
  + @return
  	* 获取到的兄弟节点
### next
```
    function next(ele) {
        var nex = ele.nextSibling;
        while (nex && nex.nodeType !== 1) {
            nex = nex.nextSibling;
        }
        return nex;
    }
```
### nextAll
```
	function nextAll(ele) {
        var nex = ele.nextSibling, ary = [];
        while (nex) {
            if(nex.nodeType === 1){
                ary.push(nex);
            }
            nex = nex.nextSibling;
        }
        return ary;
    }
```