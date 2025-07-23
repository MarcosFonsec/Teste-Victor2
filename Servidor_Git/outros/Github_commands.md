# Comandos da GitHub CLI (`gh`)

Este documento reúne os comandos mais úteis da GitHub CLI (`gh`), com uma breve explicação de cada um. Ideal para quem está começando a trabalhar com GitHub diretamente no terminal.

---

## 🔐 Autenticação

```bash
gh auth login
```
Inicia o processo de login com o GitHub, permitindo uso da CLI com sua conta.

```bash
gh auth status
```
Verifica se você está autenticado e com acesso válido.

```bash
gh auth logout
```
Desconecta sua conta da CLI.

---

## 📦 Repositórios

```bash
gh repo create NOME --public --source=. --remote=origin --push
```
Cria um novo repositório remoto com base na pasta atual.

```bash
gh repo clone USUARIO/NOME
```
Clona um repositório para seu computador.

```bash
gh repo view
```
Mostra informações sobre o repositório atual.

```bash
gh repo list USUARIO
```
Lista os repositórios públicos de um usuário.

```bash
gh repo fork
```
Faz um fork do repositório atual em sua conta.

```bash
gh repo delete
```
Exclui um repositório (confirmação interativa).

---

## 🧑‍🤝‍🧑 Colaboradores

```bash
gh api repos/USUARIO/NOME_DO_REPO/collaborators/USUARIO_COLABORADOR --method PUT -f permission=push
```
Adiciona um colaborador ao repositório com permissão de escrita (`push`).

---

## 📂 Issues

```bash
gh issue list
```
Lista as issues do repositório atual.

```bash
gh issue create
```
Cria uma nova issue (pergunta interativa).

```bash
gh issue view NUMERO
```
Visualiza os detalhes de uma issue específica.

---

## 🔀 Pull Requests

```bash
gh pr list
```
Lista os pull requests abertos no repositório.

```bash
gh pr create
```
Cria um novo pull request a partir do seu branch.

```bash
gh pr view
```
Mostra os detalhes do pull request atual.

```bash
gh pr checkout NUMERO
```
Faz checkout em um pull request (como um branch remoto).

---

## 📋 Gists

```bash
gh gist create arquivo.txt --public -d "Descrição do gist"
```
Cria um gist público com o conteúdo do arquivo.

```bash
gh gist list
```
Lista seus gists.

```bash
gh gist delete ID
```
Remove um gist.

---

## ⚙️ Configuração e Atualização

```bash
gh config set editor "code"
```
Define o VS Code como editor padrão.

```bash
gh upgrade
```
Atualiza a CLI para a versão mais recente.

---

## 🧰 Ajuda

```bash
gh help
```
Mostra ajuda geral da CLI.

```bash
gh comando --help
```
Mostra ajuda específica para o comando desejado.

---

## 📌 Observações

- Para usar os comandos da API (`gh api`), você precisa estar autenticado.
- Os comandos podem variar dependendo do sistema operacional.
- É recomendável manter a CLI sempre atualizada com `gh upgrade`.

---

## 🔗 Documentação oficial

- [Documentação GitHub CLI](https://cli.github.com/manual/)
- [Referência da API REST do GitHub](https://docs.github.com/rest)
