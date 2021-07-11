# 遇到的问题
1. 在Edge和Google浏览器中发现：
> document.getElementsByTagName("input");获取到的数组长度不一致

```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Title</title>
        <style>

        </style>
        <script>
            window.onload = function () {
                let btn = document.getElementById("btn");
                btn.onclick = function(){
                    let inputlist = document.getElementsByTagName("input");
                    console.log(inputlist[1].type)
                    inputlist[0].disabled = false;
                    inputlist[1].disabled = false;
                }
            }
        </script>
    </head>
    <body>
        <input type="checkbox" disabled="disabled" />input多选框
        <input type="submit" value="注册" disabled="disabled" />
        <button id="btn">获取inputlist</button>
    </body>
    </html>

```