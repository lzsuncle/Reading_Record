# 对象的扩展   
- 属性名表达式  
  ```
  let name = '小明';
  let obj = {
      c() {
          console.log("a");
      },
      [name]: 111
  };

  console.log(obj); // {c:f, 小明: 111}
  ```

- 新增方法  
  1. Object.assign() --- 合并两个对象，将源对象(source)的所有可枚举属性，复制到目标对象(target)
     合并顺序根据传参决定，没有展开运算符好用
  2. Object.is() --- 比较两个值是否严格相等，与严格比较符(===)的行为基本一致，返回布尔值  
    * 两个值都是 undefined
    * 两个值都是 null
    * 两个值都是 true 或者都是 false
    * 两个值都是由相同个数的祖父按照相同的顺序自称的字符串
    * 两个值指向同一个对象
    * 两个值都是数字并且： ===> 与严格比较符(===)不一样的地方  
      i. 都是正数零 +0  
      ii. 都是负零 -0  
      iii. 都是 NAN  

- 新增关于原型操作的一系列属性和方法：  
  1. \_\_proto\_\_ 属性
  2. Object.setPrototypeOf()
  3. Object.getPrototypeOf()