# Ubuntu20.10����git����

��ǩ���ո�ָ����� git �������� Ubuntu

---
Git��һ����Դ�ķֲ�ʽ�汾����ϵͳ��������Ч�����ٵش���Ӻ�С���ǳ������Ŀ�汾����Ҳ��Linus TorvaldsΪ�˰�������Linux�ں˿�����������һ������Դ��İ汾���������

## 1. �������Դ

## 2. ��װgit
```shell
sudo apt-get install -y git
```
## 3. ����git
- �����û���������
```shell
git config --global user.name "{username}"  //usernameΪgithubע���û���
git config --global user.email "{email}"    //emailΪgithubע�������
```
- �鿴git����
```shell
git config --list  //�鿴git����
```
- ����SSH
```shell
ssh-keygen -t rsa -C "{email}"
```
- �鿴������Կ
```shell
cat ~/.ssh/id_rsa.pub
```
- Github��������SSH

    ����Github��ҳ��ת��Settingsҳ�棬�������SSH and GPG Keys�����ӽ��沢����µ�SSH Key

![file-list](https://raw.githubusercontent.com/qingfusheng/material/master/image/3.png)

![file-list](https://raw.githubusercontent.com/qingfusheng/material/master/image/2.png)
## 4. git��ʹ��
### 1. git��������
```git
git remote add origin git@github.com:yeszao/dofiler.git # ����Զ��git�汾��
git pull origin master # ���ش��뼰���ٺϲ�
git push origin master # �ϴ����뼰���ٺϲ�
git fetch origin # ��Զ�̿��ȡ����

git branch # ��ʾ���з�֧
git checkout master # �л���master��֧
git checkout -b dev # �������л���dev��֧
git commit -m "first version" # �ύ

git status # �鿴״̬
git log # �鿴�ύ��ʷ

git config --global core.editor vim # ����Ĭ�ϱ༭��Ϊvim��gitĬ����nano��
git config core.ignorecase false # ���ô�Сд����
git config --global user.name "YOUR NAME" # �����û���
git config --global user.email "YOUR EMAIL ADDRESS" # ��������

git add <�ļ�·��>  # ��ָ�����ļ���ӵ��ݴ�����
git commit -m "<�ύ��������Ϣ>"  # ���ݴ����е��ļ��ύ�����زֿ⣬�����ı��༭������ô��ύ��������Ϣ
git pull origin master  # ��Զ�ֿ̲��ȡ���°汾��
git pull origin master  # �ѱ��زֿ�ķ�֧���͵�Զ�ֿ̲��ָ����֧

```
