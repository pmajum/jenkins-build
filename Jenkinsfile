podTemplate(
    label: 'mypod', 
    inheritFrom: 'default',
    containers: [
        containerTemplate(
            name: 'golang', 
            image: 'golang:1.10-alpine',
            ttyEnabled: true,
            command: 'cat'
        )
    ],
    volumes: [
        hostPathVolume(
            hostPath: '/var/run/docker.sock',
            mountPath: '/var/run/docker.sock'
        )
    ]
) {
    node('mypod') {
        
        stage('Extract'){
            try{
            sh """
            git clone 'https://github.com/pmajum/jenkins-build.git'
            """
            }catch(exc){
               println('Exception :::::::::::::::===========>>>>>>>>>>'+exc) 
            }
        }
        
        
    }
}
