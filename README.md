
# 📁 Versionamento com Git e GitHub

## 🧩 Situação-Problema

A proposta da atividade foi simular um cenário real de versionamento, onde é necessário:

- Preservar o histórico de alterações do código-fonte;
- Trabalhar em equipe conciliando diferentes alterações no mesmo repositório;
- Utilizar **Git** e **GitHub** como ferramentas principais de controle de versão.

## 🛠️ Ferramentas Utilizadas

* Editor de texto
* Conhecimentos adquiridos no curso SENAI

## 📋 Etapas Realizadas

1. ✅ Acesso ao site [git-scm.com](https://git-scm.com/downloads/win) e instalação do Git.
2. ✅ Configuração do usuário:
   ```bash
   git config --global user.name "Seu Nome"
   git config --global user.email "seu@email.com"
    ```
3. ✅ Criação de um repositório Git local com git init.
4. ✅ Criação do arquivo senai_versoes_versionameto.txt com o seguinte conteúdo:

   ```bash
   <HTML>
   <HEAD><TITLE>ATIVIDADE DE VERSIONAMENTO</TITLE></HEAD>
   <BODY>
      <H1> TÍTULO1 </H1>
   </BODY>
   </HTML>
   ```

5. ✅ Cadastro e criação de repositório remoto no GitHub.
6. ✅ Publicação inicial na branch main


## 🌱 Branches e Alterações

* ✨ Branch main alterada para:

```bash
<H1> VERSIONAMENTO </H1>
```

* 🌟 Branch feature1 alterada para:

```bash
<H1> GIT </H1>
```

## 🔄 Comandos Utilizados

 ```bash
Copy code
git status         # Verificar o status dos arquivos
git add .          # Adicionar arquivos ao stage
git commit -m ""   # Salvar mudanças com mensagem
git push           # Enviar para repositório remoto
git checkout       # Trocar de branch
git merge          # Mesclar branches
git pull           # Baixar alterações do remoto
git remote add     # Conectar ao GitHub
 ```
 
## ⚔️ Resolução de Conflito

Durante o git merge feature1 na branch main, ocorreu um conflito na linha 
   ```bash
   <HTML>
   <HEAD><TITLE>ATIVIDADE DE VERSIONAMENTO</TITLE></HEAD>
   <BODY>
   <<<<<< H1 HEAD
      <H1> GIT </H1>
   ======
      <H1> VERSIONAMENTO </H1>
   >>>>>> main
   </BODY>
   </HTML>
   ```

   ```bash
      <H1> GIT - VERSIONAMENTO </H1>
   ```
O conflito foi resolvido manualmente, optando pelo conteúdo mais apropriado para o projeto.

## 🧠 Aprendizado

* Esta atividade reforçou conceitos essenciais de versionamento:
* Diferença entre repositório local e remoto;
* Criação e gerenciamento de branches;
* Resolução de conflitos de merge;
* Uso dos principais comandos do Git no dia a dia de um desenvolvedor.
