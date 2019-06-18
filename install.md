* GCEでインスタンスを作成  
マケプレから使い慣れているCentOS7を選択して作成する。

* パッケージインストール
```
sudo yum install -y epel-release
sudo yum install -y ansible git docker

```

* awxの2.1.0をgit clone  
```
git clone https://github.com/ansible/awx.git
cd awx
git branch
devel
git checkout -b 2.1.0 tags/2.1.0

```

```
cd installer
sed -i s@postgres_data_dir=/tmp/pgdocker@postgres_data_dir=/var/lib/pgsql/data@ inventory
sed -i 's/# use_docker_compose=false/use_docker_compose=true/' inventory

```


* 実行
```
ansible-playbook -i inventory --become --ask-become-pass install.yml

```



