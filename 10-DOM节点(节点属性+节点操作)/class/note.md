


�ڵ������

  �����ڵ㣺 document.createElement(...);
  ��ӽڵ㣺 oDiv.appendChild(...);
  ɾ���ڵ㣺 oDiv.removeChild(oTr);

��ȡ�� id, className, tagName, name
   ���ڵ�: parentNode,
   �ӽڵ�: childNodes
   �ֵܽڵ㣺 previousElementSibling, previousSibling
            nextElementSibling, nextSibling

      Ԫ�ؽڵ㣺 nodeType == 1 


���ݣ�
    ��ȡ css ����  oDiv.currentStyle || getComputedStyle(oDiv)

    ��ȡ��һ��Ԫ�ؽڵ㣺 ͨ�� nextSibling ����װһ������
	getElementsByClassName �ļ���д��


Ӧ�ã� ���������ַ��١�tab�л�����񴴽�����ҳ����












# ��� #

1. �ڵ�����
2. �ڵ����



# �������� #

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


## �ڵ����� ##

```
box.attributes;      // �ڵ�����������
box.getAttribute('data-index')  // ��ȡԪ�ؽڵ����Ե�ֵ

box.setAttribute('data-index',2); // ���ýڵ������
box.removeAttribute('title') // �Ƴ��ڵ�����
```


### ��ҳ���� ###

css ��ʽ���� css �ļ���
```
<link id="link" href="css/css1.css" rel="stylesheet" type="text/css" />


<dl id="message">
	<form>
		<dt>
			<strong>���Ի������ύ��</strong>
			<input type="button" value="Ƥ��1" data-css="css1" />
			<input type="button" value="Ƥ��2" data-css="css2" />
		</dt>
		<dd>����������<input class="text" type="text" /></dd>
		<dd>�������룺<input class="text" type="password" /></dd>
		<dd>�������ԣ�<textarea></textarea></dd>
		<dd class="center"><input class="btn" type="submit" value="�ύ" /></dd>
	</form>
</dl>

```


style CSS������ʽ����ֵ

Ҫ��ȡ�ڵ� css ����ʽֵ��

IE�п�ͨ�� �ڵ����.currentStyle ���õ� ����Ӧ����ʽ����

```
var d = document.getElementById("div1");

// ����div�ڵ�� css ��ʽ�е� width ֵ
d.currentStyle.width;

// ����div�ڵ�� css ��ʽ�е� height ֵ
d.currentStyle.height;
```


�����Ҫ��ȡ css ��ʽֵ�� Firefox �� chrome �У�

��ͨ�� window.getComputedStyle(d, null) �ķ�ʽ���õ�����Ӧ�� ��ʽ����

```

var d = document.getElementById("div1");

// ����div�ڵ�� css ��ʽ�е� width ֵ
window.getComputedStyle(d, null).width

// ����div�ڵ�� css ��ʽ�е� height ֵ
window.getComputedStyle(d, null).height

```


���ݴ��룺

```
var d = document.getElementById("div1");

var obj = d.currentStyle || getComputedStyle(d, null);

// ����div�ڵ�� css ��ʽ�е� width ֵ
obj.width;

// ����div�ڵ�� css ��ʽ�е� height ֵ
obj.height;

```



### ������ ###

```
<style>
	#progress{
		position: relative;
		margin: auto;
		top: 200px;
		display: block;
		width: 200px;
		height: 20px;
		border-style: dotted;
		border-width: thin;
		border-color: darkgreen;
	}
	#filldiv{
		position:absolute;
		top: 0px;
		left: 0px;
		width: 0px;
		height: 20px;
		background: blue;
	}
	#percent{
		position: absolute;
		top: 0px;
		left: 200px;
		
	}
</style>


<div id="progress">
	<div id="filldiv"></div>
	<span id="percent">0</span>
</div>

```


## �ڵ�������� ##

DOM ���������Բ��ҽڵ㣬Ҳ���Դ����ڵ㡢���ƽڵ㡢����ڵ㡢ɾ���ڵ���滻�ڵ�

```
createElement() //����һ��Ԫ�ؽڵ�
createTextNode()  //����һ���ı��ڵ�
box.appendChild(node)  //��node�ڵ���뵽box�ڲ�����λ��
box.insertBefore(newNode, existNode)  //��newNode�ڵ���뵽exsitNode��ǰ��
box.removeChild(node) // ��box���Ƴ��ڵ�
box.replaceChild(p,h1); // h1�滻��p

box.cloneNode(true) // ��¡�ڵ�

```

### ��ӱ�� ###

```
	<style>
		table{margin-top:20px;width:100%;border:1px solid #ddd;border-collapse: collapse;}
		td{padding:5px 15px;border:1px solid #ddd;}

		/*css3���б�ɫ*/
		/*table tr:nth-child(odd){
			background-color:#efefef;
		}*/
		.odd{background-color:#fc0;}
	</style>


�У�<input type="text" id="row"> �У�<input type="text" id="col"><button>���ɱ��</button>
```

### ����и��� ###

node.cloneNode(true);

����Ϊ true���������Ҫ��¡�ڵ㼰�����ԣ��Լ����
����Ϊ false�������ֻ��Ҫ��¡�ڵ㼰����









# ��ҵ #
1. ���п��ð���

2. ��������
����ĳ����ť����ʾ�����ж�Ӧ����Ϣ


```
<style type="text/css">
* { padding: 0; margin: 0; }
li { list-style: none; }
body { background: #f6f9fc; font-family: arial; }

.calendar { width: 210px; margin: 0 auto; padding: 10px 10px 20px 20px; background: #eae9e9; }
.calendar ul { width: 210px; overflow: hidden; padding-bottom: 10px; }
.calendar li { float: left; width: 58px; height: 54px; margin: 10px 10px 0 0; border: 1px solid #fff; background: #424242; color: #fff; text-align: center; cursor: pointer; }
.calendar li h2 { font-size: 20px; padding-top: 5px; }
.calendar li p { font-size: 14px; }

.calendar .active { border: 1px solid #424242; background: #fff; color: #e84a7e; }
.calendar .active p { font-weight: bold; }

.calendar .text { width: 178px; padding: 0 10px 10px; border: 1px solid #fff; padding-top: 10px; background: #f1f1f1; color: #555; }
.calendar .text h2 {font-size: 14px; margin-bottom: 10px; }
.calendar .text p { font-size: 12px; line-height: 18px; }

</style>


	var arr=['������ˣ���ҿ���������ȥ����ɡ�',
		'��Һú�ѧϰ��222222~~~',
		'��Һú�ѧϰ��222222333~~~',
		'��Һú�ѧϰ��222444222~~~',
		'��Һú�ѧϰ555��222222~~~',
		'��Һú�ѧϰ��666222222~~~',
		'��Һú�ѧϰ��227772222~~~',
		'��Һú�ѧϰ��28888822222~~~',
		'��Һú�ѧϰ��99999222222~~~',
		'��Һú�ѧϰ10000000��222222~~~',
		'��Һú�ѧϰ��111111222222~~~',
		'��Һú�ѧϰ��22222200000000000~~~']



<div id="tab" class="calendar">

    <ul id="ul">
        <li class="active"><h2>1</h2><p>JAN</p></li>
        <li><h2>2</h2><p>FER</p></li>
        <li><h2>3</h2><p>MAR</p></li>
        <li><h2>4</h2><p>APR</p></li>
        <li><h2>5</h2><p>MAY</p></li>
        <li><h2>6</h2><p>JUN</p></li>
        <li><h2>7</h2><p>JUL</p></li>
        <li><h2>8</h2><p>AUG</p></li>
        <li><h2>9</h2><p>SEP</p></li>
        <li><h2>10</h2><p>OCT</p></li>
        <li><h2>11</h2><p>NOV</p></li>
        <li><h2>12</h2><p>DEC</p></li>
    </ul>
    
    <div class="text" id="txt">
        <h2>1�»</h2>
        <p>������ˣ���ҿ���������ȥ����ɡ�</p>
    </div>

</div>
```



2. ��ϰ֮ǰ������������


3. ����Ч��
    ![](hw1.jpg)

����չ�� ���ʱ�༭(��Ҫ�õ��¼�ð��֪ʶ)

���������ݣ����Ա༭�ı���������뿪�༭��󣬿��Խ��༭������ݱ�������



