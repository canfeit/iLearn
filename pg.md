# pg

安装存储库RPM： yum install [https://download.postgresql.org/pub/repos/yum/10/redhat/rhel-7-x86\_64/pgdg-centos10-10-1.noarch.rpm](https://download.postgresql.org/pub/repos/yum/10/redhat/rhel-7-x86_64/pgdg-centos10-10-1.noarch.rpm) 安装客户端软件包： yum install postgresql10 可选地安装服务器软件包： yum install postgresql10-server 有选择地初始化数据库并启用自动启动： /usr/pgsql-10/bin/postgresql-10-setup initdb systemctl enable postgresql-10 systemctl start postgresql-10 ln -s /usr/pgsql-10/bin/pg\_config /usr/bin/pg\_config

su - postgres psql postgres=\# \password postgres

find / -name "postgresql.conf" vi /var/lib/pgsql/10/data/postgresql.conf listen\_addresses = '\*'

vi /var/lib/pgsql/10/data/pg\_hba.conf 末尾添加 host all all 0.0.0.0/0 md5

systemctl restart postgresql-10

