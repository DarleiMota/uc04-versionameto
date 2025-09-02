# UC 04 Vesionaento

  1. [O que é Versionamento](#-o-que-%C3%A9-versionamento)
  2. [O que é Git](#-o-que-%C3%A9-git)
  3. [A Importância do GitHub](#-a-import%C3%A2ncia-do-github)
  4. [Uso de Branches](#-uso-de-branches)
  5. [Principais Comandos do Git](#-principais-comandos-do-git)
  6. [Fluxo de Trabalho Básico](#-fluxo-de-trabalho-b%C3%A1sico)
  7. [Dicas Importantes](#-dicas-importantes)
  8. [Conclusão](#-conclus%C3%A3o)
  9. [Atividade: Versionamento com Git e GitHub](#-atividade-versionamento-com-git-e-github)

-----

### **🔄 O que é Versionamento**

**Versionamento** é o processo de gerenciar e registrar as mudanças em documentos, código-fonte ou outros conjuntos de informação. No desenvolvimento de software, é uma prática fundamental que permite:

  - **Rastrear o histórico:** Cada alteração é salva com uma "versão" específica, criando um registro detalhado do que foi alterado, quando e por quem.
  - **Recuperar versões:** É possível voltar a um estado anterior do projeto para corrigir bugs ou desfazer mudanças indesejadas.
  - **Colaborar sem conflitos:** Permite que múltiplos desenvolvedores trabalhem no mesmo projeto ao mesmo tempo sem que suas mudanças se sobreponham.

### **🤔 O que é Git**

**Git** é um sistema de controle de versão **distribuído**, criado por Linus Torvalds em 2005. Ele é a principal ferramenta para realizar o versionamento de projetos de software. A principal característica do Git é que cada desenvolvedor possui uma cópia completa do histórico do repositório, o que permite trabalhar offline e garante redundância de dados.

### **⭐ A Importância do GitHub**

**GitHub** é uma plataforma de hospedagem de código-fonte baseada em Git. Ele atua como um repositório remoto que oferece funcionalidades essenciais para a colaboração:

  - **Backup e compartilhamento:** Mantém uma cópia segura do código na nuvem.
  - **Colaboração em equipe:** Permite a revisão de código e a integração de funcionalidades através de *pull requests*.
  - **Gestão de projetos:** Oferece ferramentas como *Issues* para rastrear bugs e tarefas.
  - **Portfólio profissional:** Serve como uma vitrine para desenvolvedores demonstrarem suas habilidades.

-----

### **🌿 Uso de Branches**

*Branches* (ramificações) são uma das funcionalidades mais poderosas do Git, permitindo que os desenvolvedores trabalhem em linhas de desenvolvimento paralelas.

  - **Isolamento de Mudanças:** Cada nova funcionalidade, correção de bug ou experimento pode ser desenvolvido em sua própria *branch*, mantendo a *branch* principal (*main* ou *master*) estável.
  - **Trabalho em Equipe:** Em projetos com múltiplos desenvolvedores, as *branches* permitem que cada membro trabalhe em sua tarefa simultaneamente sem interferir no trabalho dos outros.
  - **Manutenção do Histórico:** O uso de *branches* ajuda a manter um histórico de *commits* limpo e organizado na *branch* principal, que mostra apenas as mudanças que foram devidamente revisadas e testadas.
  - **Proteção do Código:** *Branches* protegem o ambiente de produção ao criar uma barreira entre o desenvolvimento ativo e o código estável.

-----

### **⚡ Principais Comandos do Git**

#### **Comandos Essenciais**

| Comando | Descrição | Exemplo |
| :--- | :--- | :--- |
| `git init` | Inicializa um novo repositório Git. | `git init` |
| `git clone` | Clona um repositório remoto para sua máquina. | `git clone https://github.com/usuario/repo.git` |
| `git add` | Adiciona arquivos modificados à área de *stage*. | `git add .` ou `git add arquivo.txt` |
| `git commit` | Salva as mudanças do *stage* no histórico. | `git commit -m "Mensagem do commit"` |
| `git status` | Mostra o status dos arquivos no repositório. | `git status` |
| `git push` | Envia os *commits* para o repositório remoto. | `git push origin main` |
| `git pull` | Busca e integra as mudanças do repositório remoto. | `git pull origin main` |

#### **Comandos de Branch**

| Comando | Descrição | Exemplo |
| :--- | :--- | :--- |
| `git branch` | Lista, cria ou deleta *branches*. | `git branch nova-feature` |
| `git checkout` | Muda para uma *branch* existente. | `git checkout main` |
| `git switch` | Alterna entre *branches* (comando mais moderno). | `git switch main` |
| `git merge` | Mescla os *commits* de uma *branch* em outra. | `git merge feature-branch` |
| `git rebase` | Reaplica *commits* em uma nova base. | `git rebase main` |

#### **Comandos de Inspeção**

| Comando | Descrição | Exemplo |
| :--- | :--- | :--- |
| `git log` | Mostra o histórico de *commits*. | `git log --oneline` |
| `git diff` | Mostra as diferenças entre arquivos. | `git diff` |
| `git show` | Exibe informações detalhadas de um *commit*. | `git show HEAD` |
| `git blame` | Mostra quem modificou cada linha de um arquivo. | `git blame arquivo.txt` |

#### **Comandos para Desfazer Alterações**

| Comando | Descrição | Exemplo |
| :--- | :--- | :--- |
| `git restore` | Desfaz alterações em arquivos que não foram *commitados*. | `git restore arquivo.txt` |
| `git reset` | Desfaz *commits* de forma local. | `git reset --soft HEAD~1` |
| `git revert` | Cria um novo *commit* para desfazer as alterações de um *commit* anterior. | `git revert HEAD` |
| `git clean` | Remove arquivos não rastreados. | `git clean -fd` |

#### **Outros Comandos Úteis**

| Comando | Descrição | Exemplo |
| :--- | :--- | :--- |
| `git stash` | Salva temporariamente mudanças não *commitadas*. | `git stash` |
| `git tag` | Gerencia tags para marcar versões. | `git tag v1.0.0` |
| `git config` | Configura opções do Git. | `git config --global user.name "Seu Nome"` |
| `git remote` | Gerencia repositórios remotos. | `git remote add origin URL` |

-----

### **🔄 Fluxo de Trabalho Básico**

```bash
# 1. Clonar um repositório existente
git clone https://github.com/usuario/repo.git

# 2. Criar uma nova branch para a sua feature
git checkout -b minha-feature

# 3. Fazer suas mudanças
# ...

# 4. Adicionar e commitar as mudanças
git add .
git commit -m "Adiciona nova feature"

# 5. Enviar a sua branch para o GitHub
git push origin minha-feature

# 6. Abrir um Pull Request no GitHub
```

### **🚨 Dicas Importantes**

  - ✨ Sempre use `git status` para verificar o estado atual do seu projeto.
  - 💡 Commite frequentemente com mensagens descritivas para manter um histórico claro.
  - 📝 Mantenha seu arquivo `.gitignore` atualizado para evitar que arquivos desnecessários sejam versionados.
  - 🔄 Faça `git pull` regularmente para manter seu repositório local sincronizado com as mudanças da equipe.

-----

### **✅ Conclusão**

O versionamento com Git e GitHub é uma habilidade fundamental no desenvolvimento de software moderno. Estas ferramentas não apenas preservam o histórico de alterações, mas também facilitam a colaboração em equipe, permitem o desenvolvimento paralelo de funcionalidades e protegem a integridade do código em produção. Dominar os conceitos de *branches*, *merge*, resolução de conflitos e fluxos de trabalho é essencial para qualquer desenvolvedor que deseja trabalhar de forma eficiente e profissional em projetos de software.

-----

### **🎯 Atividade: Versionamento com Git e GitHub**

#### **Situação-Problema**

A proposta da atividade foi simular um cenário real de versionamento, onde é necessário:

  - Preservar o histórico de alterações do código-fonte;
  - Trabalhar em equipe conciliando diferentes alterações no mesmo repositório;
  - Utilizar **Git** e **GitHub** como ferramentas principais de controle de versão.

### 🛠️ Ferramentas Utilizadas

* Editor de texto
* Conhecimentos adquiridos no curso SENAI

### 📋 Etapas Realizadas

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


### 🌱 Branches e Alterações

* ✨ Branch main alterada para:

```bash
<H1> VERSIONAMENTO </H1>
```

* 🌟 Branch feature1 alterada para:

```bash
<H1> GIT </H1>
```

### 🔄 Comandos Utilizados

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
 
### ⚔️ Resolução de Conflito

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
