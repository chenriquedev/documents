
# Publicando seu primeiro projeto
passo-a-passo

**Objetivo:** Criar um projeto local, rastrear as alterações (commits) e publicá-lo no GitHub.

>[!WARNING] Atenção
>Certificar-se de ter o git instalado na máquina

### 1.  Preparação Local e `git init`
Nesta fase, você criará a pasta do projeto e ativará o Git.

1. Crie uma pasta chamada `meu-primeiro-projeto`

2. **Inicialize o Repositório Git:** Transforme essa pasta em um repositório Git. Isso cria o banco de dados local (`.git`). Para isso, abra um terminal dentro da pasta e execute o comando:

```bash
git init
```

3. **Verifique o Status Inicial:** Use o comando para confirmar que o repositório foi criado e que está vazio.

```bash
git status
```

_Resultado:_ O Git dirá que não há _commits_ ainda.

### 2. Criando o Primeiro Commit

Você fará o primeiro **"snapshot"** do projeto.
1- **Crie o Arquivo:** **Abra seu editor de texto** (VS Code). Crie um arquivo com o conteúdo básico dentro da pasta que você criou e **salve-o** com o nome **`index.html`**

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Meu Projeto</title>
</head>
<body>
    <h1>Página Inicial</h1>
</body>
</html>
```

2-**Verifique o Status (`Modified`):** Execute o `git status` novamente para ver o novo arquivo.

```bash
git status
```
_Resultado:_ O Git dirá que o arquivo `index.html` está em **vermelho** (Untracked / Não rastreado).

3-**Prepare o Arquivo (`Staged`):** Adicione o arquivo à **Staging Area** (Área de Preparação).

```bash
git add index.html
```

4-**Verifique o Status (`Staged`):** Use o `git status` para confirmar a preparação.

```bash
git status
```
_Resultado:_ O Git mostrará o `index.html` em **verde** (Changes to be committed / Pronto para salvar).

5-**Salve o Progresso (Commit):** Salve o _snapshot_ no banco de dados local.

```bash
git commit -m "commit inicial e estrutura base HTML"
```


### 3: Criando o Segundo Commit e Usando `git log`

Agora vamos rastrear uma mudança e usar o comando de histórico.

1- **Modifique o Arquivo:** Volte ao seu editor de texto, abra o `index.html` e adicione um parágrafo.

```html
<h1>Página Inicial</h1>
<p>Esta é a primeira versao do meu projeto salvo com Git!</p>
```

2- **Verifique e Salve a Mudança:** Repita o ciclo:

```bash
git status # Mostrará Modified (vermelho)
git add index.html # Passa para Staged (verde)
git commit -m "Adiciona texto de boas-vindas na pagina inicial"
```

3- **Visualize o Histórico:** Use o comando para ver todos os _commits_ que você salvou localmente.

```bash
git log
```

_Resultado:_ Você verá dois blocos, um para o "commit inicial" e outro para o "Adiciona texto...".

### 4: Conectando ao GitHub e Publicando

Agora, você criará o repositório remoto e enviará seu trabalho.

1- **Crie o Repositório Remoto (No GitHub):**

- Crie um novo repositório no GitHub com o nome `meu-primeiro-projeto`.
- **NÃO** marque a opção de adicionar README/License.

2- **Conecte e Envie:** Copie e cole as linhas que o GitHub sugere (na seção de repositório existente) para conectar seu Git local ao remoto e enviar os dois _commits_ criados:

```bash
git remote add origin https://www.youtube.com/watch?v=X49Wz3icO3E
git branch -M main
git push -u origin main
```
_Resultado:_ Se o `push` for bem-sucedido, seus dois _commits_ e o arquivo `index.html` aparecerão no GitHub.

>[!WARNING] Atenção
>Esses 3 últimos comandos, git remote, git branch e git push, o próprio GitHub nos fornece essa informação, basta copiar.

