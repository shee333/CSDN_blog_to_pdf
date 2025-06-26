# CSDN_blog_to_pdf

##第一步：  
打开想要导出的页面，空白处点击鼠标右键⇒点击“检查”或“check”，或直接在页面按F12键。  

##第二步：  
复制以下代码粘贴到控制台，并按回车。  

若提示让输入“允许粘贴”或“allow pasting”，按提示输入后点回车键就行，输入完后再次粘贴该代码。  

allow pasting  


(function doPrint(){      
	'use strict';
	var articleBox = $("div.article_content");
	articleBox.removeAttr("style");
	var head_str = "";       
	var foot_str = "";   
	var older = document.body.innerHTML;       
	var title= document.getElementsByClassName('article-title-box')[0].innerHTML; 
	var main_body = document.getElementsByClassName('article_content')[0].innerHTML;
	document.body.innerHTML = head_str + title + main_body + foot_str;
	$("#mainBox").width("100%");
	document.getElementsByTagName('body')[0].style.zoom=0.8;     
	window.print();
	document.body.innerHTML = older;
	return false;
})();  
##第三步：  
输入代码并按回车键后，会弹出如下提示框，点击“保存”就行。  
