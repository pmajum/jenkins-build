podTemplate(
    label: 'mypod', 
    inheritFrom: 'default',
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
            checkout scm
            }catch(exc){
               println('Exception :::::::::::::::===========>>>>>>>>>>'+exc) 
            }
        }
        
        
    }
}
