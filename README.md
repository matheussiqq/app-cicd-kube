# app-cicd-kube

Pipeline com objetivo de rodar uma aplicação HTML em um cluster kubernetes.

Se atentar nos seguintes passos no .gitlab-ci.yml:
  
  Stages = no qual você irá criar de acordo com o seu projeto
  
  $REGISTRY_USER e REGISTRY_PASS = váriaveis armazenadas nas configurações do seu repositório no Gitlab
  
  deploy_gcp:
    before_script = permissão de leitura de chave privada para o Owner
    
    SSH_KEY = chave privada armazenada na variavel do repositorio
    SSH_SERVER = IP do servidor armazenado em variavel do repositorio
