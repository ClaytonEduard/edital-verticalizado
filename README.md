# TRILHA — Central de Estudos

Site estático em português para acompanhar editais, cronograma, revisão, questões, discursivas e PDFs.

**Versão atual:** CGU 2026 — AFFC, Cargo 4 (TI / Desenvolvimento de Sistemas); TCE-GO 2026/2027 — Técnico de Controle Externo, opção B02 (Tecnologia da Informação).

## O que está incluído

- `index.html`: site completo. **Não requer Node, npm, instalação de pacotes nem banco de dados.**
- `modelo-edital.txt` e `modelo-edital.json`: modelos para cadastrar novos concursos na página **Importar concurso**.
- `.nojekyll`: simplifica a publicação estática no GitHub Pages.
- `.gitignore`: ajuda a evitar publicar PDFs e backups pessoais por engano.

O conteúdo inclui **182 correlações de estudos** divididas em assuntos comuns (58), foco CGU (58) e foco TCE-GO (66). Há ainda **207 subitens oficiais da CGU**, **133 recortes temáticos do TCE-GO** (considerando a retificação de legislação institucional), calendário e 9 propostas de discursiva. As pilhas são uma **classificação estratégica**, não uma identificação literal de todas as exclusividades entre os editais.

## Publicar usando VS Code e GitHub

### 1. Preparação

1. Baixe e extraia o ZIP para uma pasta de sua preferência, por exemplo `Documentos\trilha-estudos`.
2. Abra o **VS Code** → **Arquivo → Abrir Pasta...** → selecione `trilha-estudos`.
3. Verifique que `index.html` está **na raiz** dessa pasta.
4. Para testar localmente, clique duas vezes em `index.html` ou instale a extensão *Live Server* no VS Code e use **Open with Live Server**. A publicação no GitHub Pages será feita no passo seguinte.

### 2. Crie um repositório no GitHub

1. Abra https://github.com/new.
2. Dê um nome, como `trilha-estudos`.
3. Escolha **Public** (requisito para o GitHub Pages gratuito em muitos planos; confira as opções disponíveis na sua conta).
4. Clique em **Create repository**. **Não** marque a opção para adicionar README, `.gitignore` ou licença (os arquivos já vêm neste pacote).
5. Copie a URL HTTPS do repositório. Exemplo: `https://github.com/SEU-USUARIO/trilha-estudos.git`.

### 3. Envie os arquivos pelo terminal integrado do VS Code

Abra **Terminal → Novo Terminal**. Com a pasta `trilha-estudos` aberta, rode os comandos **um por vez**:

```bash
git --version
git init
git add .
git commit -m "Primeira versao do TRILHA"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/trilha-estudos.git
git push -u origin main
```

**Substitua `SEU-USUARIO` pelo seu nome de usuário no GitHub.** O GitHub pode pedir autorização por navegador, Git Credential Manager ou um token — não cole senhas nem tokens no HTML.

Se o Git solicitar seu nome e e-mail no primeiro commit, configure-os primeiro:

```bash
git config --global user.name "Seu nome no Git"
git config --global user.email "seu-email@example.com"
```

Então repita o comando `git commit ...` e siga a sequência.

### 4. Habilite o GitHub Pages

1. Dentro do repositório, abra **Settings → Pages**.
2. Em **Build and deployment → Source**, escolha **Deploy from a branch**.
3. Em **Branch**, escolha **main** e a pasta **/(root)**.
4. Clique em **Save**.
5. Aguarde o GitHub publicar. A URL normalmente será:

`https://SEU-USUARIO.github.io/trilha-estudos/`

Você também pode conferir o andamento em **Actions** ou em **Settings → Pages**.

### 5. Atualizações futuras

Depois que mudar o `index.html` no VS Code:

```bash
git add .
git commit -m "Atualiza o painel de estudos"
git push
```

**Não use `git init` ou `git remote add origin` novamente** quando o repositório já estiver configurado.

## Perfis e salvamento

- O botão **+ Criar perfil** cria um perfil *local*. Marcar conteúdos e escrever anotações salva em `localStorage`, sob chave específica para o perfil e para a origem do site.
- Dois perfis no **mesmo navegador** têm progressos separados, mas **não há senha, autenticação nem isolamento de segurança**.
- O GitHub Pages **não salva dados de usuários no repositório**. Os dados **não são automaticamente compartilhados** entre computador, celular e navegadores.
- Use **Dados e backup → Exportar backup** e importe o arquivo JSON em outro aparelho em **Dados e backup → Restaurar** para transferir o progresso.
- Se limpar os dados do site, utilizar navegação anônima ou outro navegador, o progresso poderá desaparecer. Faça backups periódicos.
- A página e o código são públicos: **não inclua arquivos pagos, tokens, dados sigilosos nem backups JSON pessoais no GitHub**.

Para sincronização de dados automática, uma etapa futura poderia integrar autenticação e banco de dados, por exemplo Firebase ou Supabase. Um repositório GitHub Pages puro não fornece banco de dados de escrita por usuário.

## Importar novos editais

Abra a aba **Importar concurso** e selecione um `.txt` ou `.json` seguindo os modelos do pacote.

Exemplo TXT:

```txt
CONCURSO: Meu próximo concurso
DATA: 2027-06-15
DISCIPLINA: Língua Portuguesa
- Interpretação de textos
- Concordância verbal
DISCIPLINA: Banco de Dados
- SQL
- Normalização
```

O importador acrescenta um concurso **ao perfil ativo** e cria sua lista de assuntos sem excluir a CGU ou o TCE-GO. Não é um leitor universal de editais: PDFs e arquivos TXT totalmente livres precisam ser preparados nesse formato antes da importação.

## Biblioteca de PDFs

- No tópico, use **Detalhes → Nome da aula / material** e **Link para o PDF**.
- Prefira PDFs com o nome **`completo`** (como `aula-00-somente-em-pdf-completo.pdf`).
- Caso a CGU não tenha disponibilizado o arquivo, marque **Ainda não liberado**.
- O link da pasta principal do Drive pode ser salvo no perfil, em **Biblioteca de PDFs**, sem ir para o código público.
- A página não busca automaticamente arquivos dentro do Google Drive: isso exigiria uma integração autenticada, ou uma importação de um catálogo JSON com os links.

## Fontes de conteúdo

- CGU: edital de 2026, conhecimentos básicos (15.2.2), complementares (15.2.3) e Cargo 4 — Desenvolvimento de Sistemas (15.2.4).
- TCE-GO: Edital nº 01/2026, Anexo II, especialidade B02, e Edital nº 02/2026 de Retificação (distribuição de questões e legislação institucional).

A correlação pedagógica entre os assuntos é uma organização de estudo criada a partir das fontes, sujeita a revisão; não equivale à classificação expressa pelas bancas.
