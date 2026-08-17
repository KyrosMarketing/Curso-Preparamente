# Curso Preparamente — Landing Page

Landing page do Curso Preparamente.

## Tecnologia

HTML, CSS e JavaScript puros — sem framework nem build step.

## Como executar localmente

Basta abrir o `index.html` no navegador, ou rodar um servidor local:

```bash
npm run dev
```

Isso sobe um servidor estático em `http://localhost:3000` (via `npx serve`).

## Como fazer build

Não há etapa de build — os arquivos estáticos (`index.html`, CSS, JS) são publicados como estão.

## Como publicar

O deploy é feito pela integração nativa de Git do hPanel (Hostinger): a cada `git push` na branch `main`, o Hostinger puxa o repositório automaticamente e atualiza o site. Detalhes em [DEPLOY.md](DEPLOY.md).

## Estrutura do projeto

```
.
├── index.html          # landing page do curso
├── assets/
│   ├── css/style.css   # estilos (tokens, layout, componentes)
│   ├── js/main.js      # menu mobile, scroll reveal, FAQ, sticky CTA
│   └── img/            # fotos, logos e favicon (ativos reais do cliente)
├── README.md
├── DEPLOY.md           # guia de publicação
└── package.json        # apenas script de dev local
```

## Fluxo Git recomendado

1. Criar uma branch a partir de `main` para cada alteração (ou commitar direto em `main` para mudanças pequenas, a critério do time).
2. Commitar com mensagens curtas e descritivas.
3. Dar `push` para o GitHub.
4. O Hostinger publica automaticamente a partir da branch `main`.

```bash
git add .
git commit -m "descrição da alteração"
git push origin main
```
