pipeline{
    agent any 
    parameters{
        string(name: 'CASE', defaultValue: '', description: 'Choisir le test a cibler')
        choice(name: 'PARCOURS', choices: ['parcours1', 'parcours2','regression' ], description: 'Choisir un type de test ou parcours')
    }
    stages{
        stage('test'){
            steps{
                script{
                    if (params.CASE == ''){
                        sh "./${params.PARCOURS}.sh"
                    }
            
                    else{
                        sh "./${params.CASE}.sh"
                    }
                }
            }
        }
       
    }
}