# Django_blog
步骤：
 A：
  定义数据模型models.py，定义post类，设置表中每一个变量
  python manage.py makemigration 创建数据库跟Django的中间文件
  python manage.py migrate 同步更新数据库内容
 B:
  python manage.py createsuperuser  创建管理界面
  在admin.py中将post纳入管理（admin.site.register）
  runserver即可进入登陆界面，成功登陆后能发表博客
  在admin.py中 定义Postadmin（admin.MOdelAdmin）让文章显示日期，时间
 C:
  在view.py中导入自定义的Model，创建homepage（request）函数
  使用Post.object.all()获取所有数据项
  返回HttpResponse（）
  在urls.p导入views.py 的homepage函数 并以url对应
 D:
  前端布局 
