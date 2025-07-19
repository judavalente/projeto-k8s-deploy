# Projeto Kubernetes: Deploy de Aplicação Fullstack

Projeto desenvolvido para a disciplina de **Virtualização** do curso de **Redes de Computadores** do IFPB - Campus João Pessoa.

## 💡 Objetivo

O objetivo deste projeto é demonstrar o deploy completo de uma aplicação web (frontend + backend + banco de dados) em um cluster Kubernetes utilizando boas práticas como:

- Configuração com `ConfigMap` e `Secret`
- Uso de `StatefulSet` para o banco de dados
- Deploy com `Deployment` e `Service`
- Exposição por `Ingress`
- Persistência de dados com `Volume`

---

## 👥 Equipe

- Judá Valente  
- João Weslley

---

## 🚀 Como Executar o Projeto

### 1. Clonar este repositório

```bash
git clone https://github.com/judavalente/projeto-k8s-deploy.git
cd projeto-k8s-deploy
```

### 2. Criar um cluster Kubernetes com o Kind

Você pode usar o Kind ou outra ferramenta de sua preferência. Para criar o cluster com o Kind:

```bash
kind create cluster --config kind-config.yaml
```

> ⚠️ Certifique-se de ter o Kind e o kubectl instalados.

### 3. Aplicar todos os manifests YAML

Acesse cada pasta do projeto e aplique os arquivos:

```bash
kubectl apply -f .
```

Ou use um script que automatize isso, se estiver disponível no projeto.

### 4. Adicionar a URL ao arquivo `/etc/hosts`

Edite seu arquivo `/etc/hosts` (como root) para associar o domínio local à sua máquina:

```
127.0.0.1  app-projeto.com
```

> No Linux:  
```bash
sudo nano /etc/hosts
```

### 5. Acessar a aplicação

Após o deploy completo e configuração do Ingress, acesse a aplicação no navegador:

👉 [http://app-projeto.com](http://app-projeto.com)

---

## 🛠 Tecnologias Utilizadas

- Kubernetes
- Docker
- React (Frontend)
- Flask (Backend)
- PostgreSQL (Banco de Dados)
- Kind (Kubernetes local)
- Ingress NGINX

---

## 📂 Estrutura do Projeto

```
projeto-k8s-deploy/
├── backend/
├── frontend/
├── database/
├── ingress/
└── namespace.yaml
```

Cada diretório contém os manifests YAML para os respectivos componentes da aplicação.

---

## 📄 Licença

Este projeto é apenas para fins educacionais no contexto da disciplina de Virtualização do IFPB.
