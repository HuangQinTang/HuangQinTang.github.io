---
layout: self
title: 留言板
subtitle: 欢迎给我留言
---
<div class="content">
    <h1 style="text-align: center">留言板</h1>
    <ul id="abc">
        <li>你好呀!</li>
        <li>第二条留言</li>
    </ul>
    <p class="last"><button id="send">发表留言</button></p>
</div>
<div id="e">
    <form action="">
        <textarea  id="editor" style="width:600px;height:300px;margin: 0 auto;margin-top: 50px;" name="message"></textarea>
    </form>
    <button class="button">确定发送</button>		
</div>


<script>
	$(function(){
		var ue = UE.getEditor('editor');
		$('#e').addClass('off');
		$('#send').click(function(){
			$('#e').toggleClass('off');
		})
		$('.button').click(function(){
			var text = UE.getEditor('editor').getContentTxt();
			$('#abc').append("<li>"+text+"</li>")
			alert("添加成功");
			ue.setContent('');
		})
	})
</script>