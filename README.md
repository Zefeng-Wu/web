## web
### PHP array to js array
    <?php
    $ar = array('apple', 'orange', 'banana', 'strawberry');
    echo json_encode($ar); // ["apple","orange","banana","strawberry"]
    ?>



## Django web (python+Django+mysql+bootstrap)
    1. 安装pycharm，创建django项目，配置conda
    2. 打开terminal，创建App:
        (Django_symbiosisDB) wuzefeng@wuzefeng-Precision-5820-Tower:~/Documents/数据库/Django_symbiosisDB$ python3 manage.py startapp gene_expression
        (Django_symbiosisDB) wuzefeng@wuzefeng-Precision-5820-Tower:~/Documents/数据库/Django_symbiosisDB$ python3 manage.py startapp Home
        (Django_symbiosisDB) wuzefeng@wuzefeng-Precision-5820-Tower:~/Documents/数据库/Django_symbiosisDB$ python3 manage.py startapp Tools
        (Django_symbiosisDB) wuzefeng@wuzefeng-Precision-5820-Tower:~/Documents/数据库/Django_symbiosisDB$ python3 manage.py startapp Genomes
        (Django_symbiosisDB) wuzefeng@wuzefeng-Precision-5820-Tower:~/Documents/数据库/Django_symbiosisDB$ python3 manage.py startapp Expression
        (Django_symbiosisDB) wuzefeng@wuzefeng-Precision-5820-Tower:~/Documents/数据库/Django_symbiosisDB$ python3 manage.py startapp Network
        (Django_symbiosisDB) wuzefeng@wuzefeng-Precision-5820-Tower:~/Documents/数据库/Django_symbiosisDB$ python3 manage.py startapp Download
        (Django_symbiosisDB) wuzefeng@wuzefeng-Precision-5820-Tower:~/Documents/数据库/Django_symbiosisDB$ python3 manage.py startapp Contact
        (Django_symbiosisDB) wuzefeng@wuzefeng-Precision-5820-Tower:~/Documents/数据库/Django_symbiosisDB$ python3 manage.py startapp Search
        
        
        简单解释一下这几个文件:
            init.py:这是一个初始化的空文件，一般我们不需要动它。
            settings.py: 这是一个配置文件，里面有关于语言、时区、安装的app声明等等信息； （主项目路径下只有一个）
            urls.py: 这个文件里指明了在访问一个页面时要调用的视图啊等的映射，确保在访问时可以正确定位到你要实现的功能；
            wsgi.py: 这是一个关于web程序的wsgi的相关配置，我们暂时不需要修改它。
            manage.py: 可以理解为他是django应用的控制中心，许多命令的实现，都需要他来调动。
  
    3. 在主目录中注册app 打开左上侧项目文件夹；打开与项目名称一致的文件夹 打开其中的setting.py 如下
        INSTALLED_APPS = [
        "django.contrib.admin",
        "django.contrib.auth",
        "django.contrib.contenttypes",
        "django.contrib.sessions",
        "django.contrib.messages",
        "django.contrib.staticfiles",
        "Home.apps.HomeConfig",
        "Tools.apps.ToolsConfig",
        "Genomes.apps.GenomesConfig",
        "Expression.apps.ExpressionConfig",
        "Network.apps.NetworkConfig",
        "Download.apps.DownloadConfig",
        "Contact.apps.ContactConfig",
        "Search.apps.SearchConfig",
                                ]
    4.视图的创建
        模版创建，所谓模版即前端界面：打开Template文件夹。新建html文件
    4.5 引入static文件，包括css和js
        在项目文件夹里创建一个名为static的文件夹，在此之前需要去setting.py引入
        
        
        接下来就是重头戏啦，配置view.py视图配置。如图。 其他五个views也按此进行配置（我这个是简易的，render的具体用法请百度，一般可将第三个参数设为redirect，就可自由跳转，否则前端界面可能跳转不畅）
        5.配置URL：URL非常重要，配置之前应理清思路配置url 打开主目录的url.py文件夹
