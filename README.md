HANDS-ON: Validador de CPF com Azure Serverless

📌 Desafio de Projeto

O objetivo deste desafio prático é criar uma aplicação para validação de CPF utilizando Azure Serverless Functions com .NET 8 Isolated.

🚀 Tecnologias Utilizadas

Azure Functions (Serverless)

.NET 8 Isolated

C#

Visual Studio Code

Git e GitHub


🛠️ Configurando o Ambiente

1️⃣ Instalar Dependências

Instale o Visual Studio Code.

Instale a extensão Azure Functions no VS Code.

2️⃣ Criar o Projeto

No VS Code, abra o terminal e execute:

mkdir hands-on-cpf-validator
cd hands-on-cpf-validator

Pressione Ctrl + Shift + P e selecione Azure Functions: Create Functions App in Azure...

Escolha sua assinatura do Azure e dê um nome para o projeto.

Selecione .NET 8 Isolated como a linguagem.

Escolha a localização e aguarde a estrutura ser criada.

3️⃣ Criar a Função HTTP

No terminal, execute:

mkdir httpValidaCpf
cd httpValidaCpf
func init --worker-runtime dotnet

Dentro da pasta criada, execute:

func new

Escolha HttpTrigger e dê um nome para a função.

4️⃣ Executar a Função Localmente

func start

Após iniciar, acesse a API localmente através do link gerado.

✅ Implementação da Validação de CPF

A validação do CPF será feita utilizando um algoritmo que verifica a estrutura e os dígitos verificadores. O código será gerado via GitHub Copilot e refinado conforme os testes.

🛠️ Solução de Erros

Durante os testes, alguns erros comuns podem ocorrer:

Erro de tipo de variável: Altere var para string onde necessário.

Erro de fechamento de chaves: Certifique-se de que todas as chaves {} estão corretamente fechadas.

Erro Not Found no método GET: Verifique se a API está rodando corretamente.

Erro ao testar POST: Acesse Body -> RAW -> JSON e envie:

{
  "cpf": "123.456.789-09"
}

🌍 Publicação no Azure

No Azure Portal, vá para Subscription -> All -> Selecione a Janela do VS Code -> Apply.

No VS Code, configure a aplicação para .NET 8 Isolated.

Corrija possíveis erros de configuração.

Copie o link gerado e teste a API.

🔑 Configuração de Chaves de Acesso

No Azure Portal, vá para Functions -> App Keys.

Copie a chave default.

No ambiente de teste, insira a chave nos parâmetros.

📜 Licença

Este projeto está sob a licença MIT.
