
# ��� #
1. window ����
2. �ص�����ʵ��
3. �޸Ĵ���

# ���� #

## BOM���� ##

JavaScript ��3�� ��ɲ���

1. ECMAScript �涨���﷨����
2. BOM  Broswer Object Model ���������ģ��
3. DOM  Document Object Model ������ҳ�ϵ�Ԫ��

### ʲô�� BOM ###


BOM ��Browser Object Model����д��������������ģ��, �ṩ�˶��������ݶ�����������ڽ��н����Ķ������ڷ���������Ĺ��ܡ�BOM��һϵ����صĶ��󹹳ɣ�����ÿ�������ṩ�˺ܶ෽��������.
JavaScript�﷨�ı�׼����֯��ECMA��DOM�ı�׼����֯��W3C, ����BOMȱ����׼.����BOM ȱ�ٹ淶��ÿ��������ṩ���ְ����Լ��뷨ȥ��չ������ô��������ж���ͳ�����ʵ�ı�׼��



(1) ����ͨ�� BOM �����������һЩ������ �򿪴��ڣ���ת������һ����ҳ ��
(2) ���е�һ������

window��BOM�ĺ���, window�����ʾ��������ڵ�һ��ʵ��, ÿ����������ڶ���һ��window������֮��Ӧ. 
window������BOM�Ķ���(����)�������ж�����ͨ�������������.

![](BOM.png)


#### ���󴴽� ####

```
1. ʹ�� new ��������� Object 
var box = new Object();        //new��ʽ  
box.name =��������;   	//���������ֶ�    
box.age = 18;		//���������ֶ�
 

2. ʹ����������ʽ���� Object 
var box = {               //��������ʽ 
      name :������',   //���������ֶ�,���Ӷ��� 
      age : 18 
};


3. �����ֶ�Ҳ����ʹ���ַ�����ʽ 
   var box={ 
	'name' : '����', 	//Ҳ�������ַ�����ʽ 
	'age' : 28
   };



4.  ʹ������������ͳ��ֵ��ʽ 
var box={};		 //��������ʽ�����յĶ���
box.name='����'; 	 //����Ÿ����Ը�ֵ
box.age= 18;



5.  �������������ʽ 
alert(box.age);		 //���ʾ����� 
alert(box['age']); 	 //�����ű�ʾ�������ע������
```



#### ������ϰ ####

1, ����һ���˵Ķ���, �������: ���� ���� ���� н������, ����һ����ӡ������Ϣ�ķ���, �������������Ϣ;



2, ����һ�����Ӷ���, ������:��,��,��; ����:���Դ�����


3, ��һ��50km/h��,����һ��1000km·�ϣ��ʶ���Сʱ���ꣿ



## window���� ##

### window������Ӷ��� ###

document(����): �ĵ����������ǿ�����js�ű���ֱ�ӷ���ҳ��Ԫ��(DOM) 
history(��Ҫ): ��ʷ����,�������ڵ������ʷ������ʵ�ֺ���
location(��Ҫ): �����������ǰ�ĵ�ַ��Ϣ����������ˢ�±�ҳ�����ת����ҳ��
frames: ��ܶ��󣬿��Ի�ȡҳ��������
screen: �����йؿͻ�����ʾ��Ļ����Ϣ
navigator: ��������, ���������йط��������������Ϣ


### ���ַ��� ###

alert(text): ������ʾ��(�����)
confirm(): ����һ����Ҫ�û�ȷ�ϵĶԻ���
prompt(text,defaultInput) :����һ���Ի���Ҫ���û�������Ϣ
open(url,name,[options]) : ��һ���´��ڲ������� window ����
setInterval(): ���ö�ʱ��
clearInterval() : �Ƴ���ʱ��
setTimeOut() : ������ʱ��
clearTimeOut(): �Ƴ���ʱ��

close(): �رմ���
print(): ������ӡ�Ի���



### location���� ###

location��BOM����֮һ�����ṩ���뵱ǰ�����м��ص��ĵ��йص���Ϣ, ���ṩ��һЩ�������ܡ�
��ʵ�ϣ�location������window��������ԣ�Ҳ��document���������; ����window.location��document.location��Ч��

location ���������

![](location.png)




Location����ķ���

![](location2.png)





## ���� ##

### ͼƬ�л� ###
�ֲ�ͼƬ�л�

1. ��ʱ����
2. ����ƶ���ͼ��ֹͣ����


### �ӳٹر���ʾ ###

���� ��ʾ ��ť������ʾ
���� ���� ��ť�󣬸�5�����ʧ


���ܣ�

�ƶ��� ��ʾ ��ť����ʾ ���ݿ�
�Ƴ� ��ʾ ��ť�� ��5��� ���� ���ݿ�


�������ݿ�֮����� �ӳ�ִ�� �Ķ�ʱ��
�Ƴ����ݿ�֮���������ݿ�
```
	<style>
#box{display:none;margin:10px 0;padding:10px;border:1px solid #ddd;font-size:30px;}
	</style>


<button id="btn1">��ʾ</button>
<button id="btn2">����</button>
<div id="box">#box</div>
```


### С��� ###

```
// ����С����
var myWindow = window.open("", "", "width=200px; height=200px");
// ��С������д������
myWindow.document.write("LoL !!!");


// �������ƶ��� (x, y) ����
myWindow.moveTo(_x, _y);
// �ڴ��ڴ�С�����ϣ�x�������� _x, y�������� _y
myWindow.moveBy(_x, _y);

// �����ڴ�С�޸ĳ� width = x, height = y;
myWindow.resizeTo(_x, _y);
// �ڴ��ڴ�С�����ϣ�������� _x, �߶� ����_y
myWindow.resizeBy(_x, _y);
```



### �ص����� ###

```
// ������ʱ����ִ�д˺���
window.onscroll = function () {
}

// IE �л�ȡ���������붥���ľ���
document.documentElement.scrollTop;


// chrome, firefox �л�ȡ���������붥���ľ���
document.body.scrollTop

```

������ݵİ취

``` 
document.documentElement.scrollTop || document.body.scrollTop || 0;
```




```
#top{display:none;position:fixed;right:0;bottom:0;padding:10px;background-color:#f00;color:#fff;}

<input type="text" id="pos">
<button id="toTop">����ָ��������λ��</button>
```








# ��� #

1. DOM���
2. �ڵ��ϵ
3. �ڵ������


# �������� #

## DOM���ĵ�����ģ�ͣ� ##

Document Object Model �ĵ�����ģ��

DOM����Document  Object Model��DOM �� W3C����ά�����ˣ��ı�׼��
W3C�ĵ�����ģ�ͣ�DOM����������ƽ̨�����ԵĽӿڣ����������ͽű���̬�ط��ʺ͸����ĵ������ݡ��ṹ����ʽ��

HTML-ҳ��ṹ   css-ҳ����ʽ    javascript �Cҳ����Ϊ����.


DOM�� ÿһ����ǩ -> ����

�������ƶ���ָͬһ�����ݣ�ֻ��˵����һ������

```
��ǩ <span> <div>     (css ��)
Ԫ�� <div id="div1">  (js ��)
�ڵ� <div> <span>     (DOM ��)
```


DOM �е�������ĸ:
D���ĵ�Document���������Ϊ����Web���ص���ҳ�ĵ���
O������Object���������Ϊ����window����֮��Ķ��������Ե������Ժͷ�������������˵���� document ����
M��ģ��Model���������Ϊ��ҳ�ĵ������ͽṹ��

ͨ�� DOM�����Է������е� HTML Ԫ�أ���ͬ�������������ı������ԡ����Զ����е����ݽ����޸ĺ�ɾ����ͬʱҲ���Դ����µ�Ԫ��


![](jd.png)

### �ڵ����� ###
Ԫ�ؽڵ�  nodeType ==1 
���Խڵ�  nodeType ==2 
�ı��ڵ�  nodeType ==3





### ��ȡ�ڵ� ###

1. id
    getElementById

2. ��ȡ��ͬ���ƵĽڵ��б� name
    getElementsByName
	ĳЩ�Ͱ汾��������м���������

3. ��ȡ��ͬclass���ԵĽڵ��б� class 
    getElementsByClassName
	IE8���²�����

```

// ��� IE �²�ͬ��ȡͬһ className �İ취

// ˼·
// 1. ���Ȼ�ȡ��ҳ�����еĽڵ�
// 2. ɸѡ�ڵ��� class == className �Ľڵ�
// 3. ������洢���������Ľڵ㣬������
function m1(a) {

	var allNode = document.getElementsByTagName("*");

	var arr = [];

	for (var i = 0; i < allNode.length; i++) {
		// ÿһ���ڵ��и��ڲ������� className
		// ����ǰ�ڵ�� class ��ֵ

		// node.onclick
		// node.style
		// node.class // ==> ��Ϊ class �Ǹ��ؼ��֣�
		// ��ȡ�ڵ�� class ��ֵ�� className

		if (allNode[i].className == a) {
			arr.push(allNode[i]);
		}
	}

	return arr;

}

```

4. tagname
    getElementsByTagName
	

```
    <h1>DOM�ṹ</h1>
    <ul id="list">
        <li><a href="http://www.baidu.com" class="baidu" id="baidu">�ٶ�</a></li>
    </ul>
    <table id="dataList">
        <tbody>
            <tr>
                <td>Data11</td>
                <td>Data12</td>
            </tr>
            <tr>
                <td>Data21</td>
                <td>Data22</td>
            </tr>
        </tbody>
    </table>

    <form>
        <input type="text" name="username" id="username">
        <input type="text" name="password" id="password">
    </form>

```


## ���� ##

### ���������ť������ ###

```
// Ϊʲôû��д���ĵ�����֮��Ϊʲô allBtn ��Ϊ��
// ��Ϊ getElementsByTagName �����ڵò���Ԫ�ص�����£�
// ��Ȼ�᷵��һ������, ֻ��������������е�Ԫ�ظ���Ϊ 0
// alert(allBtn);
```


```
// �±�Ϊ i �Ķ��� �����˺ܶ����� �� �ܶ෽���������ǿ���������������������ԣ�����
// ���±�Ϊ i �İ�ť���� ��������һ������ xxx���������е�ֵ����Ϊ i
allBtn[i].xxx = i;
```



ͨ���󶨺����ĵķ���������ȡ�����ť���±�
```
function bind(obj, pos) {
	obj.onclick = function() {
		alert(pos);
	}
}

bind(allBtn[i], i);
```





```
	<button>��ť1</button>
	<button>��ť2</button>
	<button>��ť3</button>
	<button>��ť4</button>
	<button>��ť5</button>
	<button>��ť6</button>
```

### tab��ǩ�л� ###

```
#tab span{display:inline-block;padding:5px 15px;background-color:#ddd;margin:0 3px;border:1px solid #ddd;border-bottom:none;}
.content{padding:15px;border:1px solid #ddd;font-size:24px;background-color:#efefef;}



<div id="tab"><span>����</span><span>����</span><span>������</span><span>�����׷�</span></div>
<div class="content">��ϲ��������</div>
<div class="content">���궹��������</div>
<div class="content">ϲ��ȥ�����󷽱���</div>
<div class="content">�����׷�����������</div>

```


## �ڵ�֮��Ĺ�ϵ ##

�ӽڵ�: childNodes

���ڵ�: parentNode

�ֵܽڵ�:
    nextSibling
	previousSibling



```
		// �ٶ�Ԫ�ص���һ����Ԫ�ء��ڵ�
		// ��֧�� IE8������
		// baidu.previousElementSibling.style.color = "red";

		// �������IE ���ݵ�����
		// ֻҪ��ǰ�ڵ㲻��Ԫ�ؽڵ㣬��ôһֱ������
		while (google.nodeType != 1) {
			google = google.previousSibling;
		}
```


### ���б�ɫ ###

![](ghbs.png)

```
<style>
.red{background:red;}
</style>


<ul id="ul01">
	<li>A</li>
    <li>B</li>
    <li>C</li>
    <li>D</li>
    <li>E</li>
    <li>F</li>
</ul>

```



### ���ڵ��Ӧ�� ###

```
<style>
  a {cursor: pointer;}
</style>

<h1> ����ͷ�� </h1>

<ul id="ul1">
	<li>�һ�Ѳ���Ϻ��ͷ��ش��ź� ��6��ͻ������������  <a>&times;</a></li>
	<li>�������Լ��ſ�����ɮ����NBA����Τ�°ݷ�Ĳ�������... <a>&times;</a></li>
	<li>���ǿ̸������+���������Ƿ�չ�¾��ã�����������ͳ.. <a>&times;</a></li>
	<li>��λ85�����У�Ҫʵ��APP֮����������  <a>&times;</a></li>
	<li>���������ñ�ӹر� ���²�  <a>&times;</a></li>
</ul>

```


### �ַ��� ###


```
<style>
		.hide{display:none;}

		#div1{border:1px solid #ddd;padding:1px;}
		#div1 h4{margin:1px;background-color:#ddd;padding:15px;}
		#div1 .content{display:none;height:120px;padding:15px;}
</style>

	<div id="div1">
		<h4>����1</h4>
		<div class="content">#����1</div>
		<h4>����2</h4>
		<div class="content">#����2</div>
		<h4>����3</h4>
		<div class="content">#����3</div>
		<h4>����4</h4>
		<div class="content">#����4</div>
		<h4>����5</h4>
		<div class="content">#����5</div>
	</div>


```


# �������� #

1. ��������ô���дһ��
2. ��洰���Զ��ر�, ����ʱ5���رմ��� (�ֱ�ʹ�ö�ʱ������ʱ��)
![](close.png)

3. ��������,�����������������·�ʱ, ������Ϣһֱ��ʾ�ڶ���
![](top1.png)
![](top2.png)


4. ��ȡ�����ַ��Ĳ�����ת���ɶ����ʽ
	?name=green&age=18&school=ǧ��&class=h5����&lesson=javascript



3. ȫѡ�ͷ�ѡchecked


![](checked1.png)
![](checked2.png)


```
	<table id="dataList">
		<thead>
			<th><input type="checkbox" name="all" id="all"></th>
			<th>����</th>
		</thead>
		<tbody>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>��ë��</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>��ɽ</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>��Ӿ</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����Ӱ</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����</td>
			</tr>
		</tbody>
	</table>
```





# BOM���� #


BOM:

���ĵĶ��� window


��������� �� var res = window.prompt("�ú�������Ĵ���")
ȷ�Ͽ� var res = window.confirm("ȷ��?")

��ʱ�ظ�ִ�У� var res = window.setInterval(����, ʱ��); 
����ظ�ִ��   window.clearInterval(res);

��ʱִ�У� var res = setTimeout(����, ʱ��)
�����ʱ�� clearTimeout(res)


�򿪴��ڣ� var res = window.open(��ַ, ���ƣ�ѡ��)
�ô����ƶ���  res.moveTo(x, y);           moveBy
�ô��ڱ���С��  res.resizeTo(x, y);      resizeBy


// ��IE ���������붥���ľ���
document.body.scrollTop

// IE ���������붥���ľ���
document.documentElement.scrollTop;


// ����д��
var t = document.body.scrollTop || document.documentElement.scrollTop;


����ʱ��������
window.onscroll = function() {}

ҳ��������ִ�к���
window.onload = function() {}


������İ汾
window.navigator.appName
window.navigator.userAgent

��ȡ��ǰ������ַ�� location.href
��ȡ��ַ�в�ѯ�ַ����� location.seach

ˢ�£� location.reload()
     location.reload(true)

ǰ���� history.forward();
���ˣ� history.back();
��¼������ history.length


-------------
DOM


ͨ��id��ȡ�ڵ����  var obj = document.getElementById("id");
ͨ����ǩ����ȡ���нڵ����  var all = document.getElementsByTagName("div");
ͨ��name����ȡ���нڵ���� var all = document.getElementByName("username");


this








