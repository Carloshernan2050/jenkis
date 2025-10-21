pipeline{
    agent any

    stages {
        stage('Instalar dependencias') { // Instalar dependencias de Python
            steps {
                sh '''
                    python -m venv venv
                    .\venv\Scripts\activate
                    pip install -r requirements.txt || echo "No hay dependencias para instalar"
                '''
            }
        }

        stage('Ejecutar pruebas') {
            steps {
                sh '''
                    .\venv\Scripts\activate
                    python3 test_main.py
                '''
            }
        }   

}