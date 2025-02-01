### 🔹 **Configuração Inicial**

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@email.com"
git config --global init.defaultBranch main  # Define o branch principal como "main"
```

Verifique as configurações:

```bash
git config --list
```

---

### 🔹 **Criar ou Clonar um Repositório**

Criar um novo repositório:

```bash
git init  # Inicializa o Git no diretório atual
```

Clonar um repositório existente:

```bash
git clone https://github.com/user/repo.git
```

---

### 🔹 **Adicionar e Confirmar Alterações**

```bash
git status  # Verificar status dos arquivos
git add .  # Adicionar todos os arquivos ao stage
git commit -m "Mensagem do commit"  # Criar um commit
```

---

### 🔹 **Enviar para o Repositório Remoto**

```bash
git remote add origin https://github.com/user/repo.git  # Conectar ao remoto
git push -u origin main  # Enviar mudanças para o branch main
```

---

### 🔹 **Baixar Atualizações do Repositório**

```bash
git pull origin main  # Puxa as últimas alterações do branch principal
git fetch  # Baixa as mudanças sem mesclar automaticamente
```

---

### 🔹 **Trabalhando com Branches**

Criar e trocar de branch:

```bash
git branch nova-feature  # Criar um novo branch
git checkout nova-feature  # Mudar para o branch
git checkout -b nova-feature  # Criar e mudar para o branch
```

Mesclar um branch na main:

```bash
git checkout main  # Voltar para a branch principal
git merge nova-feature  # Mesclar as alterações
```

Deletar um branch:

```bash
git branch -d nova-feature  # Deleta localmente
git push origin --delete nova-feature  # Deleta no repositório remoto
```

---

### 🔹 **Reverter e Corrigir Erros**

Voltar ao último commit:

```bash
git checkout -- arquivo.txt  # Desfaz alterações locais em um arquivo específico
git reset --hard HEAD  # Remove todas as alterações não commitadas
```

Reverter um commit específico:

```bash
git revert <ID_DO_COMMIT>  # Cria um novo commit revertendo mudanças
git reset --soft HEAD~1  # Remove o último commit, mas mantém as mudanças no stage
```

---

### 🔹 **Trabalhando com Tags**

Criar uma tag:

```bash
git tag -a v1.0 -m "Versão 1.0"
git push origin v1.0  # Enviar a tag para o repositório remoto
```

Listar tags:

```bash
git tag
```

Deletar uma tag:

```bash
git tag -d v1.0  # Localmente
git push origin --delete v1.0  # Remotamente
```

---

### 🔹 **Ignorar Arquivos (Criar `.gitignore`)**

Exemplo de `.gitignore`:

```plaintext
node_modules/
dist/
.env
```

---

### 🔹 **Ver Histórico e Diferenças**

```bash
git log  # Histórico de commits
git log --oneline --graph  # Exibir commits resumidos
git diff  # Mostrar diferenças entre arquivos
```

---

### 🔹 **Trabalhando com Stash (Guardar Alterações Temporariamente)**

```bash
git stash  # Guardar mudanças não commitadas
git stash pop  # Recuperar mudanças guardadas
git stash list  # Listar stashes salvos
git stash drop  # Deletar um stash específico
```

---

### 🔹 **Rebase vs Merge**

- `git merge`: Mantém o histórico de commits separado, criando um "commit de merge".
- `git rebase`: Reaplica os commits da branch no topo da base atual, deixando o histórico linear.

Exemplo de rebase:

```bash
git checkout minha-feature
git rebase main
```
