
# Git
Git


touch README.md		//创建

git init		//初始化

git add README.md	//添加

git commit -m "first commit" //commit本地

git remote add orgin https://github.com/fazhongxu/ZxingDemo.git    //远程remote 源头orgin

git push -u origin master

//Push an existing repository from the command line

git remote add orgin https://github.com/fazhongxu/ZxingDemo.git

git pull orgin master //先pull再 push

git push -u origin master

git add . //添加整个目录

git commit -m "commit message"

git clone https://github.com/fazhongxu/MVPDemo.git

//Readme.md不在本地 执行 git push -u orgin master失败

可以通过如下命令进行代码合并 [注：pull=fetch+merge]

git pull --rebase origin master

git remote rm origin //移除现有仓库地址

![image](https://imageUrl)           //![image] (url)  README 里面添加图片 把括号里面的imageUrl替换为自己的图片所在的地址就可显示了

git status //查看文件当前管理状态

git 更新.gitignore文件 

vim .gitignore 编辑好要忽略的文件之后保存

git rm -r --cached .   //注意有.        清除缓存区

git add .

git commit -m "update gitignore"

git branch //查看分支

git checkout <name> //拉取分支

git tag v1.0.0 // tag v1.0.0

git push origin v1.0.0 // tag push 

git pull

git push

git stash 正在工作的项目代码 暂存

git stash list 列出存储的代码

git stash pop 出栈第一个 会删除存储的对应出栈的代码

git stash apply stash@{index} 出栈 不会删除存储的对应出栈的代码 index 为 git stash list 列出的索引

git reset HEAD~ 撤销commit 

git checkout -b (branch) feature/develop  创建并切换到 feature/develop 分支

git branch -d (或者 －D 强制删除） feature/develop 

git push orgin :feature/develop  删除远程分支




### Markdown 语法

# 这是一级标题 用 # 一直到6级标题 ######
## 这是二级标题

### 下面是java代码块  ``` java代码 ```
 ``` 
  public static <T> T checkNotNull(T reference, String errorMessage) {
    if (reference == null) {
      throw new NullPointerException(errorMessage);
    }
    return reference;
  }
```

### 下面是但行java代码

`throw new IllegalArgumentException("errorMessageTemplate has no format specifiers");`

这是*斜体*  

这是**加粗**  

这是分割线 三个 ---  或者 三个 *** 

---

***

### 这是无序列表 -+* 都可以

* 无序列表1

+ 无序列表2

- 无序列表3


### 这是有序列表 数字加上. 跟上内容即可

1. 有序列表1

2. 有序列表2

3. 有序列表3，注意点后有一个空格

### 有序无序列表嵌套

1. 有序一级内容
      * 无序二级内容
      
      + 无序二级内容 前面三个空格号就好了

### 表格

#### 表格1 

姓名|技能|排行
---|---|---|

#### 表格2

姓名|技能|排行
--|---|--|
刘备|哭|老大
关羽|打|老二
张飞|骂|老三

#### 表格3 ":" 是对齐方式  第二行 － 分割表头和内容  一个就有分割线 为了对齐多加几个

姓名|技能|排行
-|:-:|-:
刘备|哭|管他排行第几
关羽大哥|打的凶|排行老二
张飞|骂人厉害|第三



#### 服务端wiki编写格式

# 电影 余额不足提醒API

编写者:xxxx

联系方式:`xxx@qq.com` / `1000000000000'

## 余额不足提醒API

#### API 地址及校验信息：

```
    测试地址：https://www.xxx.com
    正式环境地址：https://www.xxx.com
```

正式环境请联系后获取详细内容

```
   接口地址：xxxx
```
#### 请求方式：POST

#### 传入参数：

 序号|字段名称|是否必传|类型|备注
 ---|-------|-------|---|---
 1  |pid    |yes    |string|合作方ID
 2  |version|yes    |string|接口版本，默认v1
 3  |timestamp|yes  |long  |时间戳
 4  |sinatrue|yes   |string|签名
 5  |format  |yes   |string|返回类型，json
 6  |account |yes   |string|充值手机号
 7  |shop    |no    |string|标识
 
#### 响应

```
    {
      "code ": 0,
      "msg": "发送余额不足提醒短信完成",
      "data" {
        "phone": "10000000000"
      }
    }
```



/***
 *                    .::::.
 *                  .::::::::.
 *                 :::::::::::  
 *             ..:::::::::::'
 *           '::::::::::::'
 *             .::::::::::
 *        '::::::::::::::..
 *             ..::::::::::::.
 *           ``::::::::::::::::
 *            ::::``:::::::::'        .:::.
 *           ::::'   ':::::'       .::::::::.
 *         .::::'      ::::     .:::::::'::::.
 *        .:::'       :::::  .:::::::::' ':::::.
 *       .::'        :::::.:::::::::'      ':::::.
 *      .::'         ::::::::::::::'         ``::::.
 *  ...:::           ::::::::::::'              ``::.
 * ```` ':.          ':::::::::'                  ::::..
 *                    '.:::::'                    ':'````..
 */


/***                                                                          
 *          .,:,,,                                        .::,,,::.          
 *        .::::,,;;,                                  .,;;:,,....:i:         
 *        :i,.::::,;i:.      ....,,:::::::::,....   .;i:,.  ......;i.        
 *        :;..:::;::::i;,,:::;:,,,,,,,,,,..,.,,:::iri:. .,:irsr:,.;i.        
 *        ;;..,::::;;;;ri,,,.                    ..,,:;s1s1ssrr;,.;r,        
 *        :;. ,::;ii;:,     . ...................     .;iirri;;;,,;i,        
 *        ,i. .;ri:.   ... ............................  .,,:;:,,,;i:        
 *        :s,.;r:... ....................................... .::;::s;        
 *        ,1r::. .............,,,.,,:,,........................,;iir;        
 *        ,s;...........     ..::.,;:,,.          ...............,;1s        
 *       :i,..,.              .,:,,::,.          .......... .......;1,       
 *      ir,....:rrssr;:,       ,,.,::.     .r5S9989398G95hr;. ....,.:s,      
 *     ;r,..,s9855513XHAG3i   .,,,,,,,.  ,S931,.,,.;s;s&BHHA8s.,..,..:r:     
 *    :r;..rGGh,  :SAG;;G@BS:.,,,,,,,,,.r83:      hHH1sXMBHHHM3..,,,,.ir.    
 *   ,si,.1GS,   sBMAAX&MBMB5,,,,,,:,,.:&8       3@HXHBMBHBBH#X,.,,,,,,rr    
 *   ;1:,,SH:   .A@&&B#&8H#BS,,,,,,,,,.,5XS,     3@MHABM&59M#As..,,,,:,is,   
 *  .rr,,,;9&1   hBHHBB&8AMGr,,,,,,,,,,,:h&&9s;   r9&BMHBHMB9:  . .,,,,;ri.  
 *  :1:....:5&XSi;r8BMBHHA9r:,......,,,,:ii19GG88899XHHH&GSr.      ...,:rs.  
 *  ;s.     .:sS8G8GG889hi.        ....,,:;:,.:irssrriii:,.        ...,,i1,  
 *  ;1,         ..,....,,isssi;,        .,,.                      ....,.i1,  
 *  ;h:               i9HHBMBBHAX9:         .                     ...,,,rs,  
 *  ,1i..            :A#MBBBBMHB##s                             ....,,,;si.  
 *  .r1,..        ,..;3BMBBBHBB#Bh.     ..                    ....,,,,,i1;   
 *   :h;..       .,..;,1XBMMMMBXs,.,, .. :: ,.               ....,,,,,,ss.   
 *    ih: ..    .;;;, ;;:s58A3i,..    ,. ,.:,,.             ...,,,,,:,s1,    
 *    .s1,....   .,;sh,  ,iSAXs;.    ,.  ,,.i85            ...,,,,,,:i1;     
 *     .rh: ...     rXG9XBBM#M#MHAX3hss13&&HHXr         .....,,,,,,,ih;      
 *      .s5: .....    i598X&&A&AAAAAA&XG851r:       ........,,,,:,,sh;       
 *      . ihr, ...  .         ..                    ........,,,,,;11:.       
 *         ,s1i. ...  ..,,,..,,,.,,.,,.,..       ........,,.,,.;s5i.         
 *          .:s1r,......................       ..............;shs,           
 *          . .:shr:.  ....                 ..............,ishs.             
 *              .,issr;,... ...........................,is1s;.               
 *                 .,is1si;:,....................,:;ir1sr;,                  
 *                    ..:isssssrrii;::::::;;iirsssssr;:..                    
 *                         .,::iiirsssssssssrri;;:.                      
 */	
