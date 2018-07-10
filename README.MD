# 面试题
## 题目一
```
function secondLengthString(string1, string2, index){
    var sA = string1.split(' '),
    tA = string2.split(' ');
    var cache_public_string_array = [];
    sA.forEach(sItem => {
        tA.forEach(tItem => {
            if (sItem === tItem) {
                cache_public_string_array.push(tItem);
            }
        })
    })
    cache_public_string_array.sort((a, b) => a.length > b.length);
    var result = cache_public_string_array[index];
    return result || null;
}
secondLengthString(s, t, 1);
secondLengthString(s, t, 2);
secondLengthString(s, t, 1000);
```
## 题目二
```
function decomposeNumber(number) {
    var max = Math.ceil(number / 2);
    var basics_number = 1;
    var result = [];
    while (basics_number < max) {
        var start_number = basics_number;
        var cache = [];
        var total = 0;
        while (start_number <= max) {
            total += start_number;
            cache.push(start_number)
            if (total === number) {
                result.push(cache.join(' '))
                break;
            }
            start_number++;
        }
        basics_number++; 
    }
    return result.join('\n')
}
```
## 题目三
1. [简历](http://map.liyankai.com/me.html)
2. [旅行计划](http://map.liyankai.com/map.html)
