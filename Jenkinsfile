#!/usr/bin/env groovy

pipeline {

     agent any

	stages {

		stage('Git Checkout'){

			steps {

				git 'https://github.com/madhumita-kundo/docker-react.git'

				}

		}

		stage('build'){

			steps {

				sh 'docker build -t madhumita-kundo/docker-react .'

				}

		}

		stage('test'){

			steps {

				sh 'docker run madhumita-kundo/docker-react npm run test -- --coverage'

				}

		}


	}

}
