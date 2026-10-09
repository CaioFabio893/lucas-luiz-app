# Lucas • Força e Hipertrofia

Aplicativo estático para GitHub Pages, instalável na tela inicial como PWA. Sem servidor, contas ou dependências de compilação.

## Conteúdo

Estrutura de aplicativo para força e hipertrofia. A orientação de correção de assimetria foi removida. As três opções de HIIT/cardio foram mantidas. A estrutura, a ficha A/B/C/D de seis semanas, o aquecimento, o deload e os recursos do aplicativo foram mantidos conforme confirmado pelo usuário.

## Publicar no GitHub Pages

1. Envie os arquivos deste projeto para a branch `main` de `https://github.com/CaioFabio893/lucas-luiz-app`.
2. No repositório, abra **Settings → Pages → Build and deployment → Source → GitHub Actions**.
3. Abra **Actions → Publicar aplicativo do Lucas → Run workflow**, caso o envio anterior tenha ocorrido antes da configuração do Pages.
4. Após a execução bem-sucedida, o endereço esperado é **https://caiofabio893.github.io/lucas-luiz-app/**.

A automação publica apenas os arquivos públicos, excluindo a pasta `work` e este documento. Os caminhos relativos permitem hospedar na subpasta do repositório. É necessário que o GitHub Pages esteja disponível para a conta/repositório.

## Instalar no celular

Abra o endereço publicado no celular. No Android/Chrome, toque em **Instalar app** ou use o menu **Adicionar à tela inicial**. No iPhone/Safari, use **Compartilhar → Adicionar à Tela de Início**. A primeira visita requer internet; depois, a ficha fica disponível offline. É um aplicativo web instalado, sem APK ou loja.

## Vídeos

Os 25 exercícios já têm links padrão do YouTube em `data.js`, no campo `videoId`. O botão **Vídeo** abre a demonstração dentro do aplicativo. Para trocar um vídeo, use **Editar vídeo do exercício**, cole um link e salve. A alteração manual fica naquele navegador e tem prioridade sobre o padrão.

A existência dos 25 vídeos e a disponibilidade de HTML de incorporação foram conferidas pelo endpoint oEmbed do YouTube. A reprodução depende de internet, das regras do YouTube e de restrições que o autor pode alterar. Os links padrão são distribuídos a todos os celulares na publicação.

## Registros e cronômetro

Cada exercício possui **Cadastrar PR do exercício**: registre a melhor carga em kg e as repetições, e toque em **Salvar PR**. O PR é independente da semana, mostra a data do registro e pode ser atualizado. Não calcula automaticamente percentuais ou 1RM.

PRs, cargas, repetições, séries concluídas, semana e vídeos são salvos no navegador. **Exportar registros** baixa uma cópia JSON; não há sincronização nem importação automática. Limpar os dados do navegador remove os registros.

Concluir uma série configura o descanso prescrito; toque em **Iniciar**. O cronômetro permite pausar, reiniciar e ajustar os segundos. Usa o horário de término para atualizar ao retornar de uma aba em segundo plano. Som e vibração dependem do dispositivo; não há garantia de alarme com tela bloqueada. Nos descansos em faixa, usa o menor valor.

## Editar

- `data.js`: ficha completa, semanas, descanso e orientações.
- `app.js`: registros, cronômetro, vídeo e instalação.
- `styles.css`: identidade visual e adaptação ao celular.
- `manifest.webmanifest`, `icons/`: configuração de instalação.
- `sw.js`: cache offline. Ao publicar mudanças, incremente a versão do cache.
- `.github/workflows/pages.yml`: publicação no GitHub Pages.

Para pré-visualizar localmente, execute `python -m http.server 8080` na pasta e abra `http://localhost:8080`. Não abra como arquivo local: o modo offline exige localhost ou HTTPS.

## Validação realizada

Conferência da extração: quatro treinos, 25 exercícios e prescrições presentes nas seis semanas. Sintaxe de todos os arquivos JavaScript validada. Manifesto e arquivos do cache verificados. Publicação, instalação em dispositivo real e reprodução de vídeos ainda precisam ser verificadas após hospedar e escolher os links.
