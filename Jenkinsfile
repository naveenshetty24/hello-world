node
{
    stage("Checkout")
    {
        currentBuild.displayName = "1.0-SNAPSHOT"
        currentBuild.description = "multibranch pipeline"
        git clone https://github.com/naveenshetty24/hello-world.git
    }
    stage("build")
    {
        bat "mvn clean compile -DskipTest=true"
    }
    stage("test")
    {
        bat "mvn clean test"
    }
    stage("deploy")
    {
        bat "mvn clean deploy -DskipTest=true"
    }
}
