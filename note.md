#gitѧϰ�ʼ�

Git��һ�ְ汾����ϵͳ��Github��һ����վ�����û��ṩgit����

###1. Git��װ�趨
���أ�windows.gitHub.com
�趨��
	git --version  #ȷ���Ƿ�ɹ���װGit
	git config --global user.name "<Your Name>"  #�趨����
	git config --global user.email "<Youremail@example.com>"  #�趨����
	git config --global user.username <Your github Name>  #���GitHub�˺���

###2. ���Լ��ĵ����Ͻ���һ������⣨repository��
һ��repository����һ����Ŀ������������ǰ�����������ĵ����ļ���.

	mkdir test  #�½��ļ��У�Ϊ�˷��㣬��������Ϊ��Ŀ����
	cd test  #�����ļ���
	git init  #������ļ����趨��һ��git��Ŀ
	git status  #ȷ����Ŀ�Ƿ��Ѿ��Ǹ�git repository

###3. ����Ŀ�д���һ�����ļ�
�����Ѵ�����һ��test.txt�ļ����ն˽���test��Ŀ�

	git status  #�鿴�Ƿ������ı�
	git add test.txt  #�������ύ���ļ�
	git commit -m "<Your commit message>"  #�ύ��repository��������һ����̵�˵��

###4. ����Ŀ����GitHub�����洢��GitHub�������ϣ������Ŀ�ͳ���Զ�˳���⣨remote repository��
���ȵ�github.com�½�һ��repository��������ú͵����ϵĳ�����һ����.
��Դ��Ŀ�о����������ĵ���

	readme  #ͨ���������ͳ���Ĺ��ܡ�ʹ�÷����Լ���ι��ף���ʱ����CONTRIBUTING.md��˵����
	.gitignore  #Ҫ���Եĵ����嵥������Git�����汾���Ƽ�¼ʱ��Ҫ�����Щ����
	License  #��������
	git remote add <remote name>  #����remote����
	git remote set-url <remote name>  #��һ��remote�趨λַ��Window��
	git remote add origin <URL from GitHub>  #�ѵ����ϵ�repository ��remote  repository������һ����Զ�˵��Ƿݾͳ�Ϊorigin
	git remote -v  #�鿴����Щremote
	git push origin master  #��master��֧�ĳ��򴫵�originԶ��

��ַ��http://jlord.us/git-it/index.html

###5. Forks And Clones
Forks������������Ŀ������
����Ŀ����github.comλ�ã����"fork"��ť��Ȼ������˺��оͳ�����һ����Ŀ������������Ŀ�����ն��л����������䡣

	git clone <URL from GitHib>  #���أ�Clone����Ŀ������Ҫ���Ƚ�����Ŀ����
	git remote add upstream <Origin URL>  #��ԭʼ��repository����Ϊupstream����ԭʼ��Ŀ���ʱpull

###6. branch
branch�����������.

	git branch <branch name>  #�½�һ����֧��Git���Ŀǰbranch�����е��ļ���������branch��
	git checkout <branch name>  #����branch

###7. Collaborators ������Ŀ�༭Ȩ������װ
��repository��GitHubҳ�棬����ұߵ�"Settings"��ѡ��"Collaborators"��ҳ�������˺���ӡ�

###8. Pull requests
�������޸ĵ�fork�ĵ�����ԭ�������ߣ�ϣ��������ȡ����repository��GitHubҳ�棬����ұߵ�"Pull request"����������м��ɡ�
��pull request �ɹ��󣬿��԰�fork��ԭʼ��repositoryͬ����

git checkout gh-pages  #���Լ��ķ�֧merge����Ҫ��branch��gh-pages����
ע������Ҫ������Ҫmerge�ķ�֧.

	git merge <branch name>  #merge��ķ�֧����
	git branch -d <branch name>  #���Ѿ�merged��branchɾ��
	git push <remote name> --delete <branch name>  #��branch��GitHub�ϵ�fork repository��ɾ��
	git pull upstream gh-pages  #��ԭ��Ŀ��ȡ����




