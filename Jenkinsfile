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
               sleep 300
           
                
                
            }catch(exc){
                println('Exception hoyeche git checkout e ---->')
                throw(exc)
            }
        }
        
        
    }
}
