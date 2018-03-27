node {
    stage 'Checkout'
    checkout scm

    stage 'Compile'
    sh "./gradlew compileJava"

    stage 'Test'
    sh "./gradlew test"

    stage 'Build'
    sh "./gradlew build"

    stage 'Release'
    archiveArtifacts artifacts: 'build/**/*.jar', fingerprint: true
}
