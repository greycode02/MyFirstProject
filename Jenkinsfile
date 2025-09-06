# Clone your repository
git clone https://github.com/greycode02/MyFirstProject.git
cd MyFirstProject

# Create Jenkinsfile
cat > Jenkinsfile << 'EOF'
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'echo "Build completed"'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }
}
EOF

# Add, commit, and push
git add Jenkinsfile
git commit -m "Add Jenkinsfile for CI/CD pipeline"
git push origin main
