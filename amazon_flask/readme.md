---ʹ������---
������virtualenv
Linux�£� $ source venv/scripts/activate
windows�£�$ venv\scripts\activate

������
1\
--cd flaskr
--python flaskr.py
	�õ����н��Running on http://127.0.0.1:5000/
	����http://127.0.0.1:5000/
....
   Ҳ����ֱ����setting���ú�python·������pycharm������
2\
--���ʺ�ᱻ�ض���http://127.0.0.1:5000/login/
--ע����ߵ�¼�ͺ�


��flaskr�е��ļ��ṹ
|controller  #��������ʱʹ�õ�ҵ�������ࣩ
	|loginController.py  #�����¼��ע������
|models	#���ݿ�����õ���ORM��,һ����Ӧһ�ű�
	|users.py   
	|entries.py #ֻ��ʵ���ʱ������õ�
|static	#������Ҫ�õ��ľ�̬��Դ
	|css
	|js
	|images
|templates	#ģ�壬��ǰ���ļ�
	|index.html
	|login.html
|config.py	#��ܵ������ļ�
|database.py	#����Mysql
|flaskr.py	#��Ҫ�ļ�����̨��ڣ�url����
|middleware.py	#�м������url��ת֮ǰ����һЩ�������
|*.sql		#�����sql��䣬������

��ע��flaskr.py��__main__����ע������һЩʵ��sqlalchemy�������ݿ�ʱ��ĺ���������