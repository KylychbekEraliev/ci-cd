// pipeline{

//     parameters {
//   string defaultValue: 'kylychbekkk', description: 'write your name', name: 'name'
// }
//     agent any
//     stages{
//         stage('aws credentials with init') { 
//             steps {
//                     sh 'terraform init'
//             }
//         }
//                 stage('aws plan') { 
//             steps {
//                 withCredentials([[
//                     $class: 'AmazonWebServicesCredentialsBinding',
//                     credentialsId: 'terraform-pipe',
//                     accessKeyVariable: 'AWS_ACCESS_KEY_ID',
//                     secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
//                     sh 'terraform plan'
//                 }
//                 }

//             }
//                     stage('terraform apply') { 
//             steps {
//                 withCredentials([[
//                     $class: 'AmazonWebServicesCredentialsBinding',
//                     credentialsId: 'terraform-pipe',
//                     accessKeyVariable: 'AWS_ACCESS_KEY_ID',
//                     secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
//                     sh 'terraform apply --auto-approve'
//                 }

//             }
//         }
//      stage('terraform destroy') { 
//             steps {
//                 withCredentials([[
//                     $class: 'AmazonWebServicesCredentialsBinding',
//                     credentialsId: 'terraform-pipe',
//                     accessKeyVariable: 'AWS_ACCESS_KEY_ID',
//                     secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
//                     sh 'terraform destroy --auto-approve'
//                 }

//             }
//         }
//              stage('kubernetes create') { 
//             steps {
//                 withCredentials([[
//                     $class: 'AmazonWebServicesCredentialsBinding',
//                     credentialsId: 'terraform-pipe',
//                     accessKeyVariable: 'AWS_ACCESS_KEY_ID',
//                     secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
//                     sh 'aws eks update-kubeconfig --region us-east-1 --name dev-eks'
//                     sh 'kubectl create -f deployment.yaml'
//                 }

//             }
//         }

//                      stage('kubernetes apply') { 
//             steps {
//                 withCredentials([[
//                     $class: 'AmazonWebServicesCredentialsBinding',
//                     credentialsId: 'terraform-pipe',
//                     accessKeyVariable: 'AWS_ACCESS_KEY_ID',
//                     secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
//                     sh 'aws eks update-kubeconfig --region us-east-1 --name dev-eks'
//                     sh 'kubectl apply -f deployment.yaml'
//                 }

//             }
//         }









//         }
//     }
