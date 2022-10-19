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

https://upload-images.jianshu.io/upload_images/7245336-f798d7f4fd379cab.png?imageMogr2/auto-orient/strip|imageView2/2/w/792/format/webp
