pipeline
       {
       agent any
             stages
                  {
                  stage('one')
                       {
                           steps
                               {
                               echo 'Hi this is suman , writing declaritive pipeline'
                               }
                       }
                  stage('two')
                       {
                             steps
                                 {
                                 input('enter do you want to proceed?')
                                 }
                       }
                  stage('three')
                      {
                           when {   not { branch "master"
                                        }
                                }
                           
                             steps
                                 {
                                 echo "hello suman"
                                 }
                      }
                  stage('four')
                     {
                     parallel {
                              stage('Unit test') {
                                        steps {
                                               echo "running unit test"
                                              }
                                              }
                              
                              stage('Integration testing') {
                                    agent {docker{
                                              
                                              image 'ubuntu'
                                              } }
                              
                                    steps{
                                    echo "running integration testing"
                                    }
                              
                              }
                              
                             
                             
                             }
                     
                     }
                     
                  }
                  
           }
           
           
           
           
           
