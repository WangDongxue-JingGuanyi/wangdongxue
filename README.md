<!doctype html>
<html lang="en">
 <head>
  <meta charset="UTF-8">
  <title>Document</title>
 </head>
 <body>
 <h2>Javascript题目</h2>
<h3>求斐波那契数列第n个数的值。题目说明如下：</h3>
<p>1.斐波那契数列指的是这样一个数列 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55...这个数列从第3项开始，每一项都等于前两项之和。</p>
<p>2.n从1开始，例如，第1项是0，第2项是1，第4项是2。(n > 0)</p>
<p>3.请修改右边的js函数<strong style="color: red;">fib</strong>，并使得下面结果区能展示正常的结果。</p>

<h2>结果区test</h2>
<div id="result"></div>
  <script>
	function fib(n) {
		var arr=[0,1];
		if (n<=0){
			n='error! n必须是大于0的正整数';
		}else if(n==1){
			n=arr[0];
		}else if(n==2){
			n=arr[1];
		}else if(n>2){
			for(var i=2;i<n;i++){
				arr[arr.length]=arr[arr.length-1]+arr[arr.length-2]
			}
			n=arr[arr.length-1];
		}
  return n;
}

var testCases = [10, 20, 30, 100, -1, 0];
var $resultEle = document.getElementById('result');
testCases.forEach(function (n) {
  var result = fib(n);
  var $ele = document.createElement('p');
  $ele.innerHTML = '第' + n + '个数是：' + result;
  $resultEle.appendChild($ele);
});
  </script>
 </body>
</html>
