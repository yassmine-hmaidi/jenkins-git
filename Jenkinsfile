pipeline {
    agent any
    options { timestamps() }
    stages {
        stage('Cloner le dépôt') {
            steps {
                bat 'echo Clonage du dépôt Git...'
            }
        }
        stage('Étape 1 : Vérification') {
            steps {
                bat 'echo === Étape 1 : Vérification du dépôt ==='
                bat 'git status'
            }
        }
        stage('Étape 2 : Contenu du projet') {
            steps {
                bat 'echo === Étape 2 : Afficher le contenu ==='
                bat 'dir'
            }
        }
        stage('Étape 3 : Simulation déploiement') {
            steps {
                bat 'echo === Étape 3 : Simulation déploiement ==='
                bat 'echo Le fichier index.html est prêt'
            }
        }
        stage('Étape 4 : Fin') {
            steps {
                bat 'echo === Étape 4 : Fin du build ==='
                bat 'echo SUCCESS'
            }
        }
    }
    post {
        success { 
            bat 'echo Build OK' 
        }
        failure { 
            bat 'echo Build KO' 
        }
    }
}