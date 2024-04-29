name: Python application

on:
  push:
   branches: [ master ]
  pull_request:
    branches: [ master ]
      
jobs:
  build:
 
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v1
    - name: Build & Push Image
      run: |
        echo "${{ secrets.DOCKERPW }}" | docker login -u "meghzz" --password-stdin
        docker image build -t meghzz/labfat:latest .
        docker push meghzz/labfat:latest
