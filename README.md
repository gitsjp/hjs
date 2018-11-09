# hjs
#bill
##<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title></title>
<script type="text/javascript"src="https://code.jquery.com/jquery-3.3.1.min.js">

</script>
</head>
<body>
<table border="1" style="width: 600px;height: 200px;text-align: center;"align="center"id="tab1">
<tr>
<td colspan="4">瑞丰电脑清单</td>
</tr>
<tr>
<td><button id="bapp">添加</button><button id="bmove">删除</button></td>
<td><laber>电脑编号</laber><br /><input type="text" name="num" id="computer"/></td>
<td><laber>电脑IP地址</laber><br /><input type="text" name="id" id="IP"/></td>
<td><laber>使用学员</laber><br /><input type="text" name="stu" id="student"/></td>
</tr>
<tr>
<td>全选<input type="checkbox" name="checkall" id="checkall"/></td>
<td>电脑编号</td>
<td>电脑IP地址</td>
<td>使用学员</td>
</tr>

<script type="text/javascript">
$("#bapp").click(function(){
var num = $("#computer").val();
var id = $("#IP").val();
var stu = $("#student").val();
$("#tab1").append("<tr><td>"+'选择<input type="checkbox" name="cle" id=""/>'+"</td><td>"+String(num)+"</td><td>"+String(id)+"</td><td>"+String(stu)+"</td></tr>");
});
//                $("#bmove").click(function(){
//                    $("#tab1").children().first().remove()
//                });
$("#checkall").click(function(){
if($("#checkall").prop("checked") === true){
$(":checkbox").prop("checked",true);
}else{
$(":checkbox").prop("checked",false);
}
});
$("#bmove").click(function(){
var l = document.getElementsByName("cle");
for(var i = 0;i<l.length;i++){
if(l[i].checked){
l[i].parentNode.parentNode.remove();
i -= 1;
}
}
});

</script>
</table>
</body>
</html>

