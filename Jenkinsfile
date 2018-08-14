podTemplate(
    label: 'mypod', 
    inheritFrom: 'default',
    containers: [
        containerTemplate(name: 'maven', image: 'maven:3.5.4-jdk-8', ttyEnabled: true, command: 'cat',
        resourceRequestCpu: '100m',
        resourceLimitMemory: '1200Mi')
    ],
    volumes: [
        hostPathVolume(
            hostPath: '/var/run/docker.sock',
            mountPath: '/var/run/docker.sock'
        )
    ]
) {
    node('mypod') {
        def commitId
        
        stage ('Extract') {
          git([url: 'https://github.com/davidcurrie/index2018.git', branch: 'master'])
            
        }
       
        stage ('Build') {
            container('maven') {
           
            sh 'mvn --version'
          }
        }
       
    }
}
