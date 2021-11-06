node('master')

{

stage('ContinuousDownload_loans')
         {
    git 'https://github.com/sunildevops77/maven.git'
        }

stage('Continuousbuild_loans')
         {
   sh label: '', script: 'mvn package'
        }

}

