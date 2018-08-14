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
        def commitId
        def workspace
        stage ('Extract') {
            try{
            workspace = pwd()
            println('Work Space Details::::'+workspace)
           

            sh "which git"
                
                
            }catch(exc){
                println('Exception hoyeche git checkout e ---->')
                throw(exc)
            }
        }
        
        
    }
}
