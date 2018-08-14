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
             git(
                url: 'https://github.com/pmajum/jenkins-build.git',
                branch: "master"
            )
                
                
            }catch(exc){
                println('Exception hoyeche git checkout e ---->')
                throw(exc)
            }
        }
        
        
    }
}
