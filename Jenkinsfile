environment {
    PATH = "C:\\Users\\kozio\\AppData\\Local\\Programs\\Python\\Python311\\python.exe;$PATH"
}

pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
                stash(name: 'compiled-results', includes: 'sources/*.py*') 
            }
        }
    }
}