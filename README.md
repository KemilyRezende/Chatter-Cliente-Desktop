# Chatter - Cliente Desktop

Este projeto, desenvolvido na disciplina de Sistemas Distribuídos, implementa um chat em tempo real que conecta um **cliente Web** a um **cliente Desktop** utilizando **middleware em Java com RMI (Remote Method Invocation)**.

Este repositório contém exclusivamente o código do **cliente Desktop**.

  - **Cliente Web**: [link para o repositório](https://github.com/KemilyRezende/Chatter)
  - **Middleware**: [link para o repositório](https://github.com/KemilyRezende/Chatter-Middleware)

## Sobre o Projeto

O Chatter permite a troca de mensagens em tempo real entre os usuários, utilizando RMI para comunicação entre os clientes Web e Desktop.
  - **Interface Gráfica**: Desenvolvida em **Swing**, com telas intuitivas para facilitar o uso..
  - **Middleware**: Responsável pela comunicação entre os clientes via **Java RMI**.

### Funcionalidades

- Troca de mensagens em tempo real.
- Interface amigável desenvolvida em **JFrames**.

## Estrutura de Arquivos

### Cliente Desktop

O Cliente desktop é organizado de forma simples, com dois arquivos principais: 

  - **`index.java`** - Tela de login.
  - **`chatter.java`** - Tela principal do chat, onde é possível ler e enviar mensagens.

### Integração com o Middleware (RMI)

A comunicação com o middleware é feita através do arquivo `rmiDesktopInterface.java`, que permite enviar e recuperar mensagens utilizando **RMI**.

## Visualização


<p align="center">
  <img src="https://github.com/KemilyRezende/Chatter-Cliente-Desktop/blob/main/telas/login.png" alt="Tela de login">
</p>
<p align="center"><em>Tela de login</em></p>

<p align="center">
  <img src="https://github.com/KemilyRezende/Chatter-Cliente-Desktop/blob/main/telas/chat.png" alt="Tela do chat">
</p>
<p align="center"><em>Tela do chat</em></p>


## Como executar

Antes de iniciar, certifique-se de ter instalado:
  - **Java 8** ou superior.
  - **Maven**

### Passos para executar


1. Clone esse repositório e acesse a pasta:
  ```bash
    git clone https://github.com/KemilyRezende/Chatter-Cliente-Desktop.git
    cd Chatter-Cliente-Desktop/chatterDesktop
  ```

2. Compile e empacote o projeto:
  ```bash
    mvn clean compile
    mvn package
  ```

3. Execute o projeto
  ```bash
    java -jar target/chat_desktop-1.0-SNAPSHOT.jar 
  ```

### Configurações Importantes

- Para que o chat funcione corretamente, o middleware RMI precisa estar rodando. Caso contrário, não será possível enviar ou visualizar mensagens.
- O **servidor RMI** é chamado utilizando o endereço **localhost** (127.0.0.1) com a respectiva porta. Isso funciona quando o servidor e os clientes estão rodando no mesmo computador. Para rodar em dispositivos diferentes, será necessário alterar o endereço **localhost** no código-fonte (`chatter.java`) para o endereço **IP** da máquina onde o **servidor** está em execução.
