# HLIB-Novel-Downloader

### 这个是有`ChatGPT`写出的一个[`H图书馆`](https://hlib.cc)的小说下载器


# `下载 & 安装`
1. `小书签代码（不推荐）`：
```
javascript:void function(){function a(a,b,c){const d=document.createElement("button");return d.textContent=a,d.style.marginBottom="10px",d.style.padding="10px 0",d.style.border="none",d.style.backgroundColor=b,d.style.color="%23fff",d.style.cursor="pointer",d.style.width="90%25",d.style.textAlign="center",d.addEventListener("click",c),d}function b(){let a="";if(j.checked){const b=document.querySelector(".text-center.m-3");b%26%26(a+=`%23 ${b.textContent.trim()}\n\n\n`)}const b=document.getElementById("content");if(b){const c=b.querySelectorAll("p");c.forEach(b=>{a+=b.textContent.trim()+"\n"})}let d=localStorage.getItem("savedContent")||"";localStorage.setItem("savedContent",d+"\n\n"+a),sessionStorage.setItem("recentContent",a),console.log("\u5DF2\u4FDD\u5B58\u5185\u5BB9\u5230LocalStorage"),c()}function c(){const a=localStorage.getItem("savedContent");console.log("\u5F53\u524D\u4FDD\u5B58\u7684\u5185\u5BB9:",a)}const d=document.createElement("div");d.style.position="fixed",d.style.top="0",d.style.left="0",d.style.height="100%25",d.style.width="4%25",d.style.backgroundColor="%23333",d.style.color="%23fff",d.style.padding="10px 0",d.style.display="flex",d.style.flexDirection="column",d.style.alignItems="center",d.style.zIndex="9999",d.style.boxShadow="2px 0 4px rgba(0, 0, 0, 0.2)",d.style.transition="transform 0.3s ease";const e=document.createElement("button");e.textContent="\u2261",e.style.position="fixed",e.style.top="10px",e.style.left="4%25",e.style.backgroundColor="%23333",e.style.color="%23fff",e.style.border="none",e.style.padding="10px",e.style.cursor="pointer",e.style.zIndex="10000",e.style.width="4%25",e.addEventListener("click",()=>{"translateX(-100%25)"===d.style.transform%3F(d.style.transform="translateX(0)",e.style.left="4%25"):(d.style.transform="translateX(-100%25)",e.style.left="0")});const f=a("\u4FDD\u5B58","%234CAF50",b),g=a("\u6E05\u9664\u5168\u90E8","%23f44336",()=>{localStorage.removeItem("savedContent"),console.log("\u5DF2\u6E05\u9664\u6240\u6709\u4FDD\u5B58\u7684\u5185\u5BB9"),c()}),h=a("\u6E05\u9664\u6700\u8FD1","%23f44336",function a(){let b=localStorage.getItem("savedContent")||"";const d=sessionStorage.getItem("recentContent")||"";b.includes(d)%3F(b=b.replace(d,""),localStorage.setItem("savedContent",b),console.log("\u5DF2\u6E05\u9664\u6700\u8FD1\u4FDD\u5B58\u7684\u5185\u5BB9")):console.log("\u6CA1\u6709\u627E\u5230\u6700\u8FD1\u4FDD\u5B58\u7684\u5185\u5BB9"),sessionStorage.removeItem("recentContent"),c()}),i=document.createElement("label");i.textContent="\u6DFB\u52A0\u6807\u9898",i.style.marginBottom="10px",i.style.display="flex",i.style.alignItems="center",i.style.width="90%25",i.style.color="%23fff",i.style.justifyContent="center";const j=document.createElement("input");j.type="checkbox",j.style.marginRight="5px",i.prepend(j);const k=a("\u4E0B\u8F7D","%232196F3",function a(){const b=localStorage.getItem("savedContent");if(b){const d=prompt("\u8BF7\u8F93\u5165\u6587\u4EF6\u540D:",document.title)||"download.txt",e=new Blob([b],{type:"text/plain"}),f=URL.createObjectURL(e),g=document.createElement("a");g.href=f,g.download=d,document.body.appendChild(g),g.click(),document.body.removeChild(g),URL.revokeObjectURL(f),localStorage.removeItem("savedContent"),console.log("\u5DF2\u4E0B\u8F7D\u5E76\u6E05\u9664\u4FDD\u5B58\u7684\u5185\u5BB9"),c()}else console.log("\u6CA1\u6709\u4FDD\u5B58\u7684\u5185\u5BB9\u53EF\u4F9B\u4E0B\u8F7D")});let l=null;const m=document.querySelectorAll(".btn.btn-primary.py-2, .btn.btn-light.py-2.me-3");m.forEach(b=>{b.onclick%26%26(l=a("\u4E0B\u4E00\u9875","%23FF9800",b.onclick))});let n=null;const o=document.querySelector(".row.pagination.mb-3");if(o){const b=o.querySelectorAll("li");if(0<b.length){const c=1===b.length%3Fb[0].querySelector("a").href:b[1].querySelector("a").href;n=a("\u4E0B\u4E00\u7AE0","%238E44AD",()=>{window.location.href=c})}}d.appendChild(f),d.appendChild(g),d.appendChild(h),d.appendChild(i),d.appendChild(k),l%26%26d.appendChild(l),n%26%26d.appendChild(n),document.body.appendChild(d),document.body.appendChild(e),document.addEventListener("keydown",a=>{a.shiftKey%26%26"S"===a.key%3Fb():a.shiftKey%26%26"Backspace"===a.key%3F(localStorage.removeItem("savedContent"),console.log("\u5DF2\u6E05\u9664\u6240\u6709\u4FDD\u5B58\u7684\u5185\u5BB9"),c()):a.shiftKey%26%26"T"===a.key%3Fj.checked=!j.checked:a.shiftKey%26%26"N"===a.key%26%26l%3Fl.click():a.shiftKey%26%26"M"===a.key%26%26n%26%26n.click()}),function a(){l%26%26(l.style.display=0<m.length%3F"block":"none")}(),c()}();
```

2. 使用`tampermonkey`浏览器插件 （推荐）：[`油猴脚本下载地址`](https://greasyfork.org/zh-CN/scripts/497246-h%E5%9B%BE%E4%B9%A6%E9%A6%86%E7%88%AC%E8%99%AB)

# 使用说明：
## 菜单栏介绍：

页面左侧会显示一个固定的菜单栏。该菜单栏包含以下按钮：

`保存`：保存当前页面的内容到LocalStorage。

`清除全部`：清除所有已保存的内容。

`清除最近`：清除最近一次保存的内容。

`下载`：将保存的内容下载为文本文件，并清除保存的内容。

`下一页`（如果存在）：导航到下一页。

`下一章`（如果存在）：导航到下一章。

`添加标题`：勾选此选项，在保存内容时将当前页面的标题添加到内容中。

快捷键功能：

使用以下快捷键可以快速执行相应操作：

`Shift + S`：保存当前页面的小说内容。

`Shift + Backspace`：清除所有已保存的内容。

`Shift + T`：切换“添加标题”勾选框的选中状态。

`Shift + N`：导航到下一页（如果存在下一页）。

`Shift + M`：导航到下一章（如果存在下一章）。

## 详细

1. 打开一本小说阅读的`第一章的第一页`，先检查这个章节有多少页。
2. 执行脚本（tampermonkey不需要，因为tampermonkey会自动执行，此处是针对使用小书签的）。执行后会在左边看到一个侧边栏。
3. 勾选`添加标题` 或 按下`Shift + T`（保存标题，只有在第一页时才需要保存标题）
4. 按下`Shift + S`：保存当前页面的内容。
5. 如果只有一页的话，也只有一章的话，就直接按下`下载`按钮来下载所保存的txt文件
6. 如果有有下一页的话，先记住有几页。
