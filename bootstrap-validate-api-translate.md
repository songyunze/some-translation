#bootstrap-validate中文api
##用例
在通过` $(form).formValidation(options)`实例化后，可以使用两种方式调用验证插件的方法:
方式1：
```javascript
// 获取对象实例
var formValidation = $(form).data('formValidation');

// 通过对象实例调用方法
formValidation.methodName(parameters)
```
方式2:
```javascript
//通过formValidation的首个参数接收方法名，其余参数接收参数值
$(form).formValidation(methodName, parameters);
```
第一种方式返回 `FormValidation` 实例, 第二种方式返回form对象。

所以两种方式的链式调用如下:
```javascript
// 方式1
$(form)
    .data('formValidation')
    .updateStatus('birthday', 'NOT_VALIDATED')
    .validateField('birthday');

// 方式2
$(form)
    .formValidation('updateStatus', 'birthday', 'NOT_VALIDATED')
    .formValidation('validateField', 'birthday');
```
