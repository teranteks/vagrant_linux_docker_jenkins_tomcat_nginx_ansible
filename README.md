## Vagrant_Linux_Docker_Jenkins_Tomcat_Nginx_Ansible Repo
---
### INFO:
>In project was used such technologies: 
>* Vagrant
>* Jenkins
>* Linux(Ubuntu/Centos7)
>* Docker
>* Ansible
>* Tomcat
>* Nginx
>
>
>List Of Used Jenkins Plugins:
>* Pipeline
>* Git
>* GitHub
>* Ansible
>* Credentials
>* SSH Agent
>* Publish Over SSH
>* Role-based Authorization Strategy
>* Matrix Authorization Strategy
>* Pipeline: Basic Steps
>* Pipeline: Multibranch
>* Pipeline: Stage Step
>* Pipeline: Input Step
>* Pipeline: Build Step
>
> 
---
### Steps To Deploy:
1. Firstly clone repo:
    * `git clone git@github.com:teranteks/vagrant_linux_docker_jenkins_tomcat_nginx.git `

2. Next `cd` into vagrant_linux_docker_jenkins_tomcat_nginx folder and run this commmand:

     * `vagrant up`

3. After execution of previous command, you will have a VM with necessary dependencies and installed jenkins for further work.
4. Later login into Jenkins using IP:PORT, that was set by default or that your set on your own in **Vagrantfile**.
5. Creating new Jenkins jobs for nginx and tomcat setup, and use Jenkinsfile from **jenkins_pipelines**.

