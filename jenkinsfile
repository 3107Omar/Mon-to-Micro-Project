node {
    stage('CLONE SOURCE CODE')
    git branch: 'Dev', url: 'https://github.com/3107Omar/Mon-to-Micro-Project.git'
    stage('BUILD DOCKER IMAGE')
    sh label: '', script: ' docker build -t udagram-frontend ./udagram-frontend '
    stage(' Tag a new version for the image ')
    sh label: '', script: 'docker tag udagram-frontend omarzztelcocloud/udagram-frontend:v8'
    stage('PUSH IMAGE TO LOCAL REGISTRY')
    sh label: '', script: ' docker push omarzztelcocloud/udagram-frontend:v8'
}
