# Casa Prática

Site em Astro, deploy automático via GitHub -> Hostinger.

## Status

- Estrutura testada e buildando sem erro (2 páginas: Início e Organização de cozinha).
- Os produtos em `src/data/produtos.json` são **dados de exemplo**, não são
  produtos reais pesquisados. Substitua pelos itens da planilha
  `biblioteca-blocos-produto.xlsx` antes de publicar de verdade.

## Como subir isso pro GitHub usando git (linha de comando)

Ver o guia passo a passo completo na conversa com o Claude. Resumo dos comandos,
rodados dentro desta pasta no terminal:

```
git init
git add .
git commit -m "primeira versão do site"
git remote add origin <URL do repositório vazio criado no GitHub>
git branch -M main
git push -u origin main
```

Depois disso, volte na tela do Hostinger ("Importar repositório Git" ->
"Continue com GitHub"), autorize o acesso, e selecione o repositório
`casa-pratica`. O Hostinger detecta o framework Astro automaticamente.

## Como adicionar produtos novos

Edite `src/data/produtos.json` seguindo o mesmo formato das colunas da
planilha (nome, selo, preço mínimo/máximo, nota, avaliações, prós, contra,
para quem, links). Cada vez que você subir uma mudança pro GitHub
(`git push` ou reenviando o arquivo pela própria tela do GitHub), o site
atualiza sozinho.
