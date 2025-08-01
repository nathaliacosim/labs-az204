# 💻 Lab AZ-204 – Desenvolvimento de Soluções na Nuvem com Azure

Este repositório contém anotações, laboratórios práticos e comandos úteis relacionados ao meu estudo para a certificação **AZ-204: Developing Solutions for Microsoft Azure**.

---

## 📌 Comandos Úteis

Lista de comandos interessantes usados ao explorar o Azure:

### 🔸 Gerais

```bash
# Listar o ID dos grupos de recursos disponíveis
az group list --query "[].{id:name}" -o tsv

# Criar um App Service Plan gratuito
az appservice plan create --name MeuPlano --resource-group MeuGrupo --sku F1 --is-linux
```

---

📚 *Este repositório será atualizado conforme avanço nos estudos e laboratórios da certificação AZ-204.*
