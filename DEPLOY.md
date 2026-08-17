# Deploy — Hostinger (Git no hPanel)

Este projeto é publicado através da integração de Git do hPanel da Hostinger, que sincroniza automaticamente o site com a branch `main` deste repositório GitHub a cada push.

## Configuração inicial (feita uma única vez, manualmente no hPanel)

1. Acesse o **hPanel** da Hostinger e entre no site/hospedagem correto.
2. Vá em **Avançado > Git** (o nome exato pode variar: "Git", "Git Version Control" ou similar).
3. Clique em **Criar novo repositório / Connect repository**.
4. Autorize o Hostinger a acessar sua conta GitHub (OAuth), caso ainda não tenha feito isso.
5. Selecione o repositório `Curso-Preparamente` e a branch `main`.
6. Defina o diretório de destino como `public_html` (ou o diretório raiz do domínio/subdomínio configurado para este site).
7. Salve. A partir daqui, o Hostinger faz o deploy automático a cada push na branch `main` (alguns planos exigem clicar em "Deploy" manualmente após cada push — verifique se há uma opção de "auto deploy" para ativar).

## Fluxo do dia a dia

```
alteração no código → commit → push origin main → Hostinger sincroniza automaticamente
```

Nenhuma credencial (FTP, senha, token) precisa ser armazenada no repositório ou no GitHub — a integração é feita via OAuth diretamente no painel da Hostinger.

## Se a integração de Git não estiver disponível no seu plano

Alguns planos de hospedagem compartilhada da Hostinger não incluem a opção de Git no hPanel. Nesse caso, as alternativas são:
- Deploy via FTP/SFTP usando GitHub Actions (exige guardar credenciais como GitHub Secrets).
- Upload manual dos arquivos via Gerenciador de Arquivos do hPanel ou cliente FTP.

Avise se for o caso que ajusto este documento e configuro a alternativa.
