pipeline {
	agent {
		label ('built-in')
	}
	stages {
		stage ('install httpd') {
			steps {
				sh "yum install httpd -y"
			}
		}
		stage ('start httpd') {
			steps {
				sh "systemctl start httpd"
			}
		}
		stage ('deploy index') {
			steps {
				sh "cd -r index.html /var/www/html"
				sh "chmod -R 777 /var/www/html/index.html"
			}
		}
	}
}
