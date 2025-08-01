# Exercício 01: Criar um Aplicativo Web HTML Estático usando Azure Cloud Shell

Neste exercício, você vai implantar um site estático básico (HTML + CSS) do repositório oficial de exemplo no **Azure App Service** usando o comando `az webapp up` da CLI do Azure.

Você fará a implantação inicial e, depois, atualizará o código e reimplantará o aplicativo.

---

## Objetivos

* Clonar o aplicativo de exemplo
* Criar o aplicativo web no Azure
* Atualizar o aplicativo localmente e reimplantar

---

## Passo a passo

### 1. Clonar o aplicativo de exemplo

No Azure Cloud Shell ou no seu terminal local, execute:

```bash
git clone https://github.com/Azure-Samples/html-docs-hello-world.git
cd html-docs-hello-world
```

---

### 2. Criar o aplicativo web no Azure

Use o comando abaixo para criar e implantar o aplicativo no Azure App Service:

```bash
az webapp up --name <NOME_UNICO_DO_APP> --resource-group <NOME_DO_RESOURCE_GROUP> --runtime "HTML"
```

> **Importante:**
>
> * Substitua `<NOME_UNICO_DO_APP>` por um nome único para o seu app (deve ser único globalmente).
> * Substitua `<NOME_DO_RESOURCE_GROUP>` pelo nome do seu grupo de recursos (pode criar um novo com `az group create`).
> * O parâmetro `--runtime "HTML"` indica que é um app estático HTML.

Após a execução, o comando fará o deploy do app e mostrará a URL para acessar.

---

### 3. Atualizar o aplicativo e reimplantar

* Faça alterações nos arquivos HTML e CSS na pasta `html-docs-hello-world`, por exemplo no `index.html`.
* Salve as alterações.
* Reexecute o comando para atualizar o deploy:

```bash
az webapp up --name <NOME_UNICO_DO_APP> --resource-group <NOME_DO_RESOURCE_GROUP> --runtime "HTML"
```

---

## Observações

* O Azure Cloud Shell já vem com o Azure CLI instalado, então pode executar todos esses comandos direto pelo navegador.
* Caso precise criar o resource group, utilize:

```bash
az group create --name <NOME_DO_RESOURCE_GROUP> --location eastus
```

* Após o deploy, acesse o site pelo link:

```
https://<NOME_UNICO_DO_APP>.azurewebsites.net
```
