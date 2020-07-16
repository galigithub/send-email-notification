node {
    stage('Checkout') {
        checkout scm
    }
}    

def notifySonarStatus() {
    def buildStatus = currentBuild.currentResult
    
    
    emailext (
        subject: "'${buildStatus}': Job '${env.JOB_NAME} ${env.BUILD_NUMBER}'",
        body: """<p>Check console output at <a href="${env.BUILD_URL}">${env.JOB_NAME}</a></p>""",
        mimeType: "text/html",
        to: "shivakumargali83@gmail.com",
        from: "shivakumar399@gmail.com"
    )
}
