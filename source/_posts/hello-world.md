---
title: HEXO
tags: Hexo
cover: https://picx.zhimg.com/70/v2-41e1b825c51055f39c22b95777bc620b_1440w.avis?source=172ae18b&biz_tag=Post
---
# 从零开始搭建个人博客

---

我为什么要搭建个人博客？

1. 记录美好生活；
2. 提升自己的技术水平；
3. 空闲时间娱乐；

---

<font color = "red" size ="5">本博客由Github+Hexo搭建，下面我来介绍我做这个博客的全过程：</font>

## 注册GitHub

1. 首先进入[GitHub官网](https://github.com/)

2. 点击Sign up

![](https://s2.loli.net/2023/05/26/4spkv6yjKPYq2Qt.png)

3. 输入你要注册的邮箱、密码![](https://s2.loli.net/2023/05/26/w5rAt1McU8DfLZF.png)

4. Create account

![](https://s2.loli.net/2023/05/26/qJ6LpkECcez42dF.png)

5. 依次按照github的提示来做，之后就省略，不难。

## Git安装步骤

1. 进入[Git官网](https://git-scm.com/),想、点击Downloads

   ![](https://s2.loli.net/2023/05/26/XCvmpUekgtPsNc1.png)

2. 选择自己的系统

   ![](https://s2.loli.net/2023/05/26/NVbQZjwHz5kDGqx.png)

3. 选择自己的适合的版本![](https://s2.loli.net/2023/05/26/NVbQZjwHz5kDGqx.png)

​	( 国内下载的速度慢，有时候还会下载失败，我这里提供[Git-2.40.1-64-bit的安装包](https://www.aliyundrive.com/s/32emvmTN9aV) )

4. 下载完成打开

5. ![](https://s2.loli.net/2023/05/26/yl4izRvqdTBLCn1.png)

6. ![](https://s2.loli.net/2023/05/26/eNLwi4Sop3kAs8X.png)

7. ![](https://s2.loli.net/2023/05/26/FmR3fzUq6wNl91H.png)

8. ![](https://s2.loli.net/2023/05/26/uWtBQJraKdRG7Zh.png)

9. ![](https://s2.loli.net/2023/05/26/rwGlm473aKEMWvA.png)

10. ![](https://s2.loli.net/2023/05/26/D7NuTQsWAHjlrwy.png)

11. ![](https://s2.loli.net/2023/05/26/TsWILrDS98yoOGb.png)

12. ![](https://s2.loli.net/2023/05/26/Vn2f47LztITKk5p.png)

13. ![](https://s2.loli.net/2023/05/26/Bzsw2Djd7FQc8m1.png)

14. ![](https://s2.loli.net/2023/05/26/gmIUl8jCiRG2c5M.png)

15. ![](https://s2.loli.net/2023/05/26/ECMy75odNPawH3b.png)

16. ![](https://s2.loli.net/2023/05/26/SpCgHmPqcwUENIh.png)

17. ![](https://s2.loli.net/2023/05/26/nERkNgU5zpiqxSX.png)

18. ![](https://s2.loli.net/2023/05/26/NJkGvSWAt6wdFRH.png)

19. ![](https://s2.loli.net/2023/05/26/nHdCWkv5O92Sb3D.png)

20. 鼠标左击出现这种情况就可以了

    ![](https://s2.loli.net/2023/05/26/SQlBgaF2YvuLcCy.png)

21. 打开Git Bash，输入git出现这种情况就可以了

    ![](https://s2.loli.net/2023/05/26/ySnF47b2xWUaQ9i.png)

## 绑定GitHub并提交文件

1. 打开Git bash 输入ssh，查看本机是否安装SSH

   ![](https://s2.loli.net/2023/05/26/mKTCNa8wS2BYPuI.png)

2. 输入`ssh-keygen -t rsa`，指定生成秘钥，接着再点击四次回车键，生成两个文件，分别为`id_rsa`，`id_rsa.pub`，按照指定的文件位置打开`id_rsa.pub`，复制下来

   ![](https://s2.loli.net/2023/05/26/lmLI6WPkRhKiJcA.png)

3. 打开github，在settings中`SSH and GPG keys`中添加秘钥，名称加不加都行

   ![](https://s2.loli.net/2023/05/26/EesFogtycpwb3JV.png)

   ![](https://s2.loli.net/2023/05/26/MK4F9RpHiC7OxIS.png)

   

4. 验证是否成功，在Git Bash中输入`ssh -T github@github.com`进行验证

   ![](https://s2.loli.net/2023/05/26/N8KvWDrzjohAwdb.png)

   

## 安装node.js和Hexo

### 安装node.js及环境变量适配

大家可以看这篇[文章](https://blog.csdn.net/antma/article/details/86104068)，内容相当的详细

### 安装Hexo

1. 在github中新建一个仓库

   ![](D:\Desktop\笔记\图片\GWQ2IX1NctS6TVR.png)

2. 仓库名为`用户名+github.io`

   ![](https://s2.loli.net/2023/05/26/zHRwbt15yGinTIU.png)

3. 点击到仓库的settings，出现这种情况就可以了

   ![](https://s2.loli.net/2023/05/26/mevcw1kIht5UELn.png)

4. 安装Hexo：在任意一个盘符下面新建一个`Blog`文件夹打开文件夹，使用git Bash 的管理员身份运行，输入`npm install -g hexo-cli`，安装完成之后，在使用`hexo init`命令初始化一下，输入`hexo g`静态部署，输入`hexo s`可以本地预览，在浏览器中输入`localhost:4000`，就可以本地预览网页了

5. 将Hexo部署到GitHub中：打开Blog文件夹，打开`_config.yml`文件，滑到文件的最下方，修改

   ![](https://s2.loli.net/2023/05/26/at2KjYhmLPAE84k.png)

   ![](https://s2.loli.net/2023/05/26/16b3vVJNHitP4oX.png)

   ![](https://s2.loli.net/2023/05/26/fSyYRl5OIFAJhcd.png)

6. 然后回到`Blog`文件夹中，打开Git Bash，安装Git部署插件，输入命令：

   ```npm
   npm install hexo-deployer-git --save
   ```

   再输入以下的指令：

   ```hexo
   hexo clean #清除缓存文件db.json和已生成的静态文件public
   hexo g     #生成网站静态文件到默认设置的 public 文件夹(hexo generate的缩写)
   hexo d     #自动生成网站静态文件，并部署到设定的仓库(hexo deploy 的缩写)
   ```

   在浏览器中输入`你的用户名+github.io`就可以访问网站了

## 解析域名

1. 域名绝大部分是付费的，但是也有免费的，比如我的这个czlifetime.eu.org，具体的申请教程在[这](https://www.bilibili.com/video/BV1gs4y1J7xZ/?spm_id_from=333.880.my_history.page.click&vd_source=f38da837f7ffc103f340849927ff2d1f)

2. 得到域名后，在阿里云、腾讯云、华为云等可以解析，添加记录：A @ 185.199.108.153 和 A @ 185.199.109.153 和 A @ 185.199.110.153 和 A @ 185.199.111.153，任意选一个或两个就可以了

3. 打开Blog文件夹里的source文件夹，添加CNAME文件，可以先创建一个CNAME.txt文件，打开后写上你的域名，不要加www否则每次访问都必须加www，但如果不带有www，以后访问的时候带不带www都可以访问，保存后记得要重命名，将.txt删除

4. 第三步回到Blog 文件夹，右键打开Git Bash，依次输入下面三条命令:

   ```hexo
   hexo clean #清除缓存文件db.json和已生成的静态文件public
   hexo g     #生成网站静态文件到默认设置的 public 文件夹(hexo generate的缩写)
   hexo d     #自动生成网站静态文件，并部署到设定的仓库(hexo deploy 的缩写)
   ```

5. 打开GitHub，看看CNAME文件是否已经在你的项目中，如果没有，可以在github的仓库中添加，最后github中也要把你的域名写进去

   ![](https://s2.loli.net/2023/05/26/Z5SmLtMvVpyW4T3.png)

## 设置主题

### 推荐

`hexo`有很多种主题，我推荐8种主题

1. Butterfly
   + GitHub地址：https://github.com/jerryc127/hexo-theme-butterfly
   + 在线演示：https://butterfly.js.org/
2. ICARUS
   + GitHub地址：https://github.com/ppoffice/hexo-theme-icarus
   + 在线演示：https://ppoffice.github.io/hexo-theme-icarus/
3. Fluid
   + GitHub地址：https://github.com/fluid-dev/hexo-theme-fluid
   + 在线演示：[hexo.fluid-dev.com/](https://hexo.fluid-dev.com/)
4. Volantis
   + GitHub地址：https://github.com/volantis-x/hexo-theme-volantis
   + 在线演示：[volantis.js.org](https://volantis.js.org/)
5. Snippet
   + GitHub地址：https://github.com/shenliyang/hexo-theme-snippet
   + 在线演示：[snippet.shenliyang.com/](https://snippet.shenliyang.com/)
6. Hacker
   + GitHub地址：https://github.com/CodeDaraW/Hacker
   + 在线演示：[blog.daraw.cn/](https://blog.daraw.cn/)
7. 3-hexo
   + GitHub地址：https://github.com/yelog/hexo-theme-3-hexo
   + 在线演示：[yelog.org](https://yelog.org/)
8. Cactus
   + GitHub地址：https://github.com/probberechts/hexo-theme-cactus
   + 在线演示：[probberechts.github.io/hexo-theme-cactus/](https://probberechts.github.io/hexo-theme-cactus/)

### 配置

点开GitHub的地址，详细的配置就在首页的md文件中，这里不过多赘述

