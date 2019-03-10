properties([
    
    parameters([
        choice(choices: ['IL', 'CA'].join("\n"), description: 'select state', name: 'state'),
         string(defaultValue: 'Ramya', description: 'Enter your name', name: 'Name', trim: false)
        ])
        
        ])


if(state=='IL')
{
    
    j_node='master'
}       else {
    
    j_node='w4'
}

node(j_node){

stage('Build and generate .war file'){
    echo 'generated .war file'
    powershell 'mvn --version'
 sleep 4
echo "Choice: ${params.state}"
echo "Choice: ${params.Name}"

 
}

stage('Deploy code to QA'){
    echo 'deploying the .war file to QA'
    echo 'QA will test and follow the process'
   sleep 4
}

stage('Deploy to Production'){
    echo '.war file successfully deployed to Production '
}
}
