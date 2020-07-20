#1 docker jenkins镜像 

官方推荐： jenkinsci/blueocean

The recommended Docker image to use is the jenkinsci/blueocean image (from the Docker Hub repository). This image contains the current Long-Term Support (LTS) release of Jenkins (which is production-ready) bundled with all Blue Ocean plugins and features. This means that you do not need to install the Blue Ocean plugins separately.

https://github.com/jenkinsci/docker
docker run -p 8870:8080 -p 50000:50000 -v /mnt/zw-docker/jenkins/data:/var/jenkins_home jenkins/jenkins:lts
docker run -p 8870:8080 -p 50000:50000 -v /mnt/zw-docker/jenkins/data:/var/jenkins_home zhiwei-jenkins:0.1

##1.1,访问:

http://39.102.50.86:9999

http://39.102.48.153
##1.2，密码位置:

cat /var/jenkins_home/secrets/initialAdminPassword

212ac9f2ebde40069d0e6c95afe5246f



#2 jenkins pipleline
##2.1参考资料
https://www.jenkins.io/doc/book/pipeline/
##2.2 条件
(1)Jenkins 2.x 版本以上
(2) Blue Ocean UI 编辑Jenkinsfile

#!/usr/bin/env groovy

Blue Ocean Access to Github
docker2主机（安装jenkins）id_rsa.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCcWfKT6wFRgxL6Ya6D+Tx7lbbo/behRYwEA6OGDqqSEVeXjFKiPGmuPpiqsLwE3y8t2L1MlQBxDegHsyzaAc1zi/KszMxfMdnBlhL52xf4jMNGvS7CbXMg/xzVOJrADna1i/9QIutUO97cB3Gx7PS+EywdVWv/D/iEdtUwghJaKzkIuqsnBBcXMM7olH3aGrWZOZRO9nYt3N3Je73looFeDCz0kQDMbM9Vi3WYvO8tWTRzTTSN/iMt+ToltJIvH2DDkKXbxmsJRKExWVqit2fz+t+D0JLYbyBtbEkTy86W9XJd0sjGPrua/R0hWI8VsKEJMJlj/7jgsK3cIlKq1Hwj root@docker2
Generate an GitHub accessToken 
 
493114187a95be80a6fa07bb22756201951dd4e3
为什么用pipeline?

刚开始使用Jenkins的时候，大部分的使用方式都是采用FreeStyle进行构建自动化部署的配置，但是随着业务的不断增加与变化也要创建N多个Job来进行管理，甚至当服务器环境迁移之类的事情产生之后发现这种管理方式太过于低效，需要手工来维护这些大量的配置信息，并且相关配置一旦改过之后无法追溯到某个版本，还有脚本的灵活度也不高，所以后来研究使用Pipeline的方式创建Job，然后创建Jenkinsfile文件跟随项目仓库存放，这样灵活度与可追溯性大大加强，利于自动化部署更上一层台阶。
Jenkinsfile

/mnt/zw-docker/softwares/repository
/mnt/zw-docker/softwares/maven3/conf/settings.xml

docker info | grep "Docker Root Dir"   /var/lib/docker


cd /mnt/zw-docker/softwares/git

make configure
./configure --prefix=/mnt/zw-docker/softwares/git2
make all doc info
make install install-doc install-html install-info


(1) maven 外挂

/mnt/zw-docker/softwares/maven3/conf
/mnt/zw-docker/softwares/repository

几个常用的插件：
Deploy to container plugin
Maven Integration plugin
GIT plugin


Email Extension Plugin

PMD Source Code Analyzer Project

查看jenkins安装目录

ll /var/lib/jenkins/plugins/

######## PMD工程调研 ##############
https://pmd.github.io/latest/



FindBugs, PMD, Jtest

Allure 报告插件
	
Report Info 报告插件


/var/jenkins_home/workspace/pipeline/








