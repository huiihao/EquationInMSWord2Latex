# EquationInMSWord2Latex

之前有写过OCR识别公式(图片)的操作(但是被删掉了)，就是用Mathpix Snipping Tool软件，但是每个邮箱ocr公式数量有限。现在有一个github项目也可以做到：
[GitHub - blaisewang/img2latex-mathpix: An image to LaTeX tool by MathpixOCR API and JavaFX](github.com/blaisewang/img2latex-mathpix)

而对于公式(图片)转换为tex格式，操作如下。

准备：MS Office、MathType

安装步骤：
拥有Office的激活权限，最好是365版本的(有些方法只能用这个版本的)，如果用到MathType不是365版本的也可以，WPS也可以。如果没有，这边建议安装365版本破解版，这个就不写的太详细了(要被抓起来），就是Office Tool Plus软件先安装(部署)365版本，然后激活选择Mondo版本的，不是批量版似乎也可以：

![image](https://user-images.githubusercontent.com/48110180/188317770-202dfabc-fe6d-494d-9ca6-a87f9e0cd953.png)

这个版本和365的功能一样，也会跟着更新，原生365版本的证书可能会失败

接下来有两个选择来进行激活，一个是去找激活码输入，一个是用Office Tool Plus软件激活界面的KMS管理。这些操作，都可以搜到。

![image](https://user-images.githubusercontent.com/48110180/188317789-3e514b63-3439-4ec6-91f2-d749924c1b61.png)

# 而我的建议是，再去下载一个HEU KMS Activator，然后点击使用KMS激活MS Office即可。

![image](https://user-images.githubusercontent.com/48110180/188317814-a0cf223f-07ce-49eb-b5dc-5d6344413cea.png)

2. 官网下载MathType并安装，由于需要购买使用，所以可以使用试用版30天。关于到期，延长使用期限的小技巧：打开系统的##注册表编辑器##，找到**计算机\HKEY_CURRENT_USER\SOFTWARE\Install Options\Options7.4**，也可能是Options6.9等等，其对应的是MathType版本，然后选中**删除**即可。再次打开MathType，又可以继续试用30天。这个方法的局限性在于，可能会被软件开发者修复。

**公式转换方法1：**
选中word中的公式

![image](https://user-images.githubusercontent.com/48110180/188317870-9ae0bdd5-eeeb-492e-a62f-027b0c18688b.png)

快捷键**Alt+\**

![image](https://user-images.githubusercontent.com/48110180/188317888-200bc663-5d75-4126-882e-ad60b2aff603.png)

**公式转换方法2：**

![image](https://user-images.githubusercontent.com/48110180/188317908-9e7525dd-f44e-4514-a66e-ac4eb9c74503.png)

![image](https://user-images.githubusercontent.com/48110180/188317912-e997628c-13f3-4987-b61c-49b1b07be842.png)

![image](https://user-images.githubusercontent.com/48110180/188317918-ccb0e273-7710-44e0-aebb-a079f619858e.png)

将全文复制进LaTex编辑器，使用查找替换功能，将公式中的 \[ 和 \] 转化为\begin{equation}、\end{equation}

![image](https://user-images.githubusercontent.com/48110180/188564113-a0722d4a-6bb4-4c28-9215-ae1a3c02fecf.png)

比如，用Overleaf在线编辑，ctrl+f后打开正则表达式， \\代表\ ， \[代表[ ，(\n)代表换行，然后replace即可。

哦只有搜索认识正则表达式，替换不行，所以换行怎么实现呢?
