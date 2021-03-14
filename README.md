# services-k8s
Esse projeto tem como finalidade juntar todos os projetos já feitos por mim visando usar boas práticas de devOps e comunicação e estrutura de infra as code


### Serviços utilizados
- go-mongo (https://github.com/zero101010/go-mongo)
- chatbot (https://github.com/zero101010/chatbot-go)
- Api python finance (https://github.com/zero101010/chatbot-go)
- Api server analytics (https://lab.coodesh.com/igotaraujo97/api-server-analytics)
- Front api server analytics (https://lab.coodesh.com/igotaraujo97/challenge-20200714)


### Passos para a execução
#### 1- Configurar o K8S
- Para isso usaremos a digital Ocean, e depois iremos criar um ingress-nginx para servir de gateway de entrada para os serviços, para executar usaremos esse tutorial, que é bem simples explicando sobre o certmanager(https://www.digitalocean.com/community/tutorials/how-to-set-up-an-nginx-ingress-with-cert-manager-on-digitalocean-kubernetes-pt).
- Após configurar o nginx iremos configurar o certmanager, nesse caso usaremos o lets-encrypt para gerar os certificados

#### 2 - Salvar em um registry cada aplicação
- Após ter dockerizado cada aplicação iremos enviar a imagem para um resgistry, e usaremos essas imagens dentro do nosso K8S, nesse projeto usaremos o próprio dockerhub para fazer isso, podemos gerar na mão ou executar um CI para esse projeto, nesse caso usaremos um CI chamado gitlab-ci, para fazer tanto o deploy quando entrega contínua.

