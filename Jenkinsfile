stage('Docker Build') {
    steps {
        // Build the image from your Dockerfile
        sh 'docker build -t my-flask-app .'
    }
}
stage('Docker Run') {
    steps {
        // Stop the old container if it exists, then run the new one
        sh 'docker stop myapp-container || true'
        sh 'docker rm myapp-container || true'
        sh 'docker run -d -p 5000:5000 --name myapp-container my-flask-app'
    }
}
