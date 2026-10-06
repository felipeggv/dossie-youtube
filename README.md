# Dossiê de YouTube · Do e-mail à thumb

Documento de estudo. O conteúdo é cifrado com **AES-256-GCM**; a chave é derivada da senha por PBKDF2-SHA256 com 600 mil iterações.

Sem a senha, o `index.html` deste repositório é ruído: abrir o código-fonte não entrega nada.

A senha é compartilhada por canal privado. **Nunca** comitar a senha aqui.

## Como atualizar

O dossiê é gerado no repositório da base de estudo (`youtube-aprendizado`), pasta `dossie/`:

1. Na base, com o `main` atualizado: `DOSSIE_SENHA=<senha> python3 dossie/build.py`
2. Copie `dossie/saida/index.html` para este repositório, por cima do atual.
3. Commit e push: o GitHub Pages publica em seguida.

O build sorteia sal e IV novos a cada vez e confere que a página reabre com a senha antes de gravar.
As fontes embutidas (Sora, Manrope, IBM Plex Mono) seguem a licença em `LICENCAS-FONTES.md`.
