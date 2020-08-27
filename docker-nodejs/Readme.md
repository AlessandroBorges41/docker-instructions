# Escrevendo um Dockerfile simples

Dockerfile especifica o que será incluído no container de sua aplicação quando for executado. A utilização de um Dockerfile permite que você defina seu ambiente de container e evite discrepâncias com dependências ou versões de runtime.

Seguindo [https://www.digitalocean.com/community/tutorials/building-optimized-containers-for-kubernetes] estas diretrizes na construção de containers otimizados, vamos tornar nossa imagem o mais eficiente possível, minimizando o número de camadas de imagem e restringindo a função da imagem a uma única finalidade — recriar nossos arquivos da aplicação e o conteúdo estático.

### No diretório raiz do projeto

   Crie um arquivo Dockerfile:
```
$ nano Dockerfile
```

Observação.: Pode ser criado por dentro da sua IDE de trabalho, exemplo: VS Code

As imagens do Docker são criadas usando uma sucessão de imagens em camadas que são construídas umas sobre as outras. Nosso primeiro passo será adicionar a imagem base para a nossa aplicação que formará o ponto inicial da construção da aplicação.
