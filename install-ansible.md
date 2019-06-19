```
mkdir gcp_ansible

```


Ansibleのインストール

```
sudo yum install -y epel-release
sudo yum install -y ansible
ansible --version

```

Ansibleの実行に必要なコンポーネントのインストール (apache-libcloudをインストールするため、まずはpipをインストール)

```
sudo yum install -y python-pip
sudo pip install --upgrade pip
sudo pip install apache-libcloud

```

