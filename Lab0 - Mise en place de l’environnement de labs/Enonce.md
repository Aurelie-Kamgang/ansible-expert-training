1. Déployez une VM (8 Go) de préference dans le Cloud
    Si vous déployer sur amazone Linux dans le **cloud AWS**, alors vous avez un script fournit (**user-data.sh**)
2. Installez **git**, **docker** et **docker-compose**
3. Recupérez le code de l’infra se trouvant sur github: 
    url: https://github.com/diranetafen/diveintoansible-lab
4. Modifiez le fichier **docker-compose.yml** afin de rajouter la variable d’environnement suivante ; 
    - **LOCALHOST_OVERRIDE=X.X.X.X** (en remplaçant **X.X.X.X** par **l'adresse IP de votre VM**)
    
5. Ne pas oublier d'adapter les variables suivantes dans le fichier **.env**
    - CONFIG=**/home/ec2-user**/diveintoansible-lab/config
    - ANSIBLE_HOME=**/home/ec2-user**/diveintoansible-lab/ansible_home

6. Lancez la stack
    ```shell
    docker-compose up -d
    ```
7. Visitez la page <ip>:1000
