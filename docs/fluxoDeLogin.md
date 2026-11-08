# Fluxo de Login do Sistema 

A funcionalidade de login permite autenticar o usuário por meio da validação de suas credenciais e controlar o acesso às funcionalidades do sistema.

### 1. Acesso à tela de Login

Quando o usuário acessar o site ele será recepcionado pela tela de login do sistema, onde apresentará:

    - O campo “usuário” 

    - O campo “senha”

    - O botão “Entrar“ 

O usuário deve informar suas credenciais e selecionar "Entrar" ou pressionar Enter para iniciar a autenticação.

### 2. Validação das Credenciais

Após o envio das credenciais, o sistema realiza a autenticação e segue um dos caminhos:

#### Credenciais Válidas

    - O sistema permitirá o acesso.

    - Uma sessão será registrada.

    - O usuário poderá utilizar as funcionalidades disponíveis de acordo com suas permissões.

#### Credenciais Inválidas

    - O sistema recusará o acesso.

    - Uma mensagem de erro informará: “Usuário ou senha estão incorretos”.

    - A tentativa será contabilizada para possível futuro bloqueio.

### 3. Bloqueio por tentativas consecutivas

Caso o usuário informe a senha incorreta cinco vezes consecutivas o sistema irá bloquear o acesso da conta por dez minutos.

    - Durante o período de bloqueio:

    - O usuário não poderá fazer novas tentativas de acesso.

    - Uma mensagem irá informar que o acesso está temporariamente bloqueado.

    - Após o término de dez minutos, novas tentativas serão disponibilizadas.

### 4. Encerrar sessão

Ao finalizar suas atividades, o usuário poderá selecionar a opção "Encerrar sessão".

Ao selecionar essa opção:

    - A sessão atual será encerrada.

    - O usuário deixará de ter acesso às funcionalidades do sistema.

    - O sistema irá direcionar o usuário para a tela de login.

## Regras de Negócio

RN001 - O campo de usuário será obrigatório.

RN002 - O campo de senha será obrigatório.

RN003 - A senha deve possuir no mínimo 8 caracteres e ao menos um caractere especial.

RN004 - Após cinco falhas de senha consecutivas, a conta será bloqueada por dez minutos.