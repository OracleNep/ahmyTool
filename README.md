1.需要的java环境是java21，java8是无法运行的

2.保持1.txt和2.txt这些poc文件和main.jar在同目录下，不然无法读取

3.命令执行和文件上传的回显都在漏洞检测的那个日志框里

4.如果感觉检测的url明明有漏洞但是此工具检测不出来 可以尝试一下修改对应的txt文件中的poc，将请求头里HOST那一行手动加上目标ip和端口再保存，重新使用工具，因为我没写Host: {{target}}，打出去可能400。但是txt文本里默认的的whoami，1.php，123456789千万别改，代码写得比较唐，request.replace("1.php", fileName).replace("123456789", fileContent);改了就找不到了

5.填入url格式，https://221.215.48.90:44300

6.suffix参数任意文件上传漏洞文件地址 /webui/1.php，aaa_local_web_preview 任意文件上传漏洞地址在根目录（直接网址/1.php），aaa_portal_auth_local_submit远程代码执行漏洞生成的回显文件1.txt也在根目录

![2`77 CJ)Z%GNK~PZ 2UPJ(P](https://github.com/OracleNep/ahmyTool/assets/159681973/062a86ca-162d-42fd-8b23-8b1d2d7dd504)


