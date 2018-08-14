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
            echo 'Waiting 5 minutes for deployment to complete prior starting smoke testing'
            sleep 300 
            }catch(exc){
                println('Exception hoyeche git checkout e ---->')
                throw(exc)
            }
        }
        
        
    }
}
