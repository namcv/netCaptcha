netCaptcha
==========

simple angular validation captcha, generate two numbers and check if the user enter the sum of them.

in your app:
```js
angular
    .module('angularTestApp', [
        'netCaptcha'
    ]);
```

in your html:

```html
<form name="myForm">
     <div class="captcha">
         <span>{{numCapOne}} + {{numCapTwo}}</span>
     </div>
     <input type="text" ng-model="captcha" captcha name="captcha" required>
     <div ng-show="myForm.captcha.$dirty && myForm.captcha.$error.captcha">
         Captcha not valid
     </div>
     <button class="btn btn-success" ng-disabled="myForm.$invalid">submit</button>
 </form>
```

```css
.captcha {
  background: #eee;
  width:90px;
  text-align:center;
  font-size: 1.2em;
  padding:20px;
  font-weight: bold;
}


```
![Alt text](https://github.com/phpnetanel/netCaptcha/blob/master/captcha.PNG "netCaptcha")
