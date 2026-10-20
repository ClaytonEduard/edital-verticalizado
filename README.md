# TRILHA — TCE-GO TI

Aplicação estática e independente de servidor, feita para publicar no GitHub Pages.

## Implantação (VS Code + GitHub)

1. Extraia o ZIP e abra a pasta no VS Code. O arquivo `index.html` deve ficar na raiz.
2. Crie um repositório público no GitHub (por exemplo `trilha-tce-go`).
3. Execute no terminal do VS Code:

```bash
git init
git add index.html README.md
git commit -m "TRILHA TCE-GO - foco exclusivo"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/trilha-tce-go.git
git push -u origin main
```

Se o repositório já existe e possui a versão antiga, substitua o `index.html` e faça apenas `git add index.html README.md`, `git commit -m "Foco TCE GO"` e `git push`.

4. No GitHub, vá a Settings > Pages > Build and deployment > Deploy from a branch > main > / (root) > Save.
5. Aguarde o deploy e abra `https://SEU_USUARIO.github.io/trilha-tce-go/`.

## Progresso e dados

- Perfis usam `localStorage` do navegador e da origem; não sincronizam automaticamente dispositivos.
- O sistema tenta migrar os perfis da versão anterior (`trilha-v3:*`) no **mesmo endereço** do GitHub Pages.
- Em outro navegador/tablet, vá a Dados e backup > Restaurar backup e selecione o JSON v3 anterior. O perfil `Clayton Eduard` e seus registros serão recuperados.
- **Nunca envie backup pessoal JSON para um repositório público**, pois pode incluir anotações e links de materiais.
- Números de prioridade foram preservados exatamente da tabela enviada. No ciclo é possível alternar entre `1 = mais urgente` e `4 = mais urgente`; o padrão é `1 = mais urgente`.
- Conhecimentos Gerais entram diariamente no ciclo. Os pesos da FCC e a distribuição de questões estão na página inicial.
- Os 98 tópicos são da tabela personalizada; a página 'Edital oficial' exibe 133 recortes do programa oficial. A 99ª linha da tabela foi reservada à discursiva.
- O `index.html` não incorpora os PDFs pagos nem dados pessoais de backup.

## Validação rápida

1. Abra a página no GitHub Pages; em Dados e backup clique em **Testar armazenamento**.
2. Importe o backup v3 do TRILHA. Confira o nome e as matérias estudadas.
3. Marque um tópico como concluído, faça uma anotação e atualize com F5.
4. Confira o ciclo, revisões, histórico de questões e estudo de caso.

## Fontes / alertas

- Edital nº 01/2026 do TCE-GO e retificação nº 02/2026.
- O corte de habilitação na prova objetiva depende da **nota padronizada** (mínimo total 150), não de atingir 150 acertos nem de um número fixo de acertos em Gerais.
- Estudo de caso exige nota >= 50/100 e fica sujeito ao limite de correção previsto no edital.
- Este site é uma ferramenta de organização de estudos, não um serviço oficial da FCC ou do TCE-GO.
