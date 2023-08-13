#Repository Setup
-

*Cretaed a github new repository 
https://github.com/ahsanulhabib93/website.git

#application Dockerization:
-

*Have written a simple Web application (index.html)

<html>
<title>jekins ci/cd pipeline</title>
<body>
<h1>Hello World! </h1>
<h2>This is CICD pipeline<h2>
</body>
</html>


*Have written dockerfile


FROM hshar/webapp
ADD . /var/www/html

#Push index.html & dockerfile to github repo
-
git add .
git commit -m "added new"
git push --force origin master



Continuous Integration(CI):
-


Created 3 instances from GCP cloud

*Installed jenkins

sudo apt update

sudo apt install openjdk-17-jre

java -version
 
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update

sudo apt-get install jenkins

sudo systemctl start jenkins.service

sudo systemctl status jenkins

Created 3 pipeilne jobs
-job1 (Git job)
-job2 (Build job)
-deployment to prod

<img width="1439" alt="Screenshot 2023-08-14 at 1 31 39 AM" src="https://github.com/ahsanulhabib93/website/assets/82897817/bac94ab5-193c-444f-93df-c24583fdcfcf">


Outcome of CICD Pipeline:
-
Whenever any changes made on repository the jenkins job will trigger sequentially in queue
<img width="1440" alt="Screenshot 2023-08-14 at 2 02 56 AM" src="https://github.com/ahsanulhabib93/website/assets/82897817/9f395084-7357-4f4e-9d09-fee26f46fb83"><img width="1440" alt="Screenshot 2023-08-14 at 2 02 19 AM" src="https://github.com/ahsanulhabib93/website/assets/82897817/44995a3c-7446-4cec-b587-04d1f7a76722">








