---
layout: default
title: Política de Privacidade
---

# Política de Privacidade do Veo+

**Última atualização:** 25 de novembro de 2026

O Veo+ é um programa da Vecola Productions que roda **inteiramente no
computador do próprio usuário**. A Vecola Productions não opera servidor para o
Veo+, não recebe dados do programa e não tem acesso a nada do que ele
manipula.

Este documento existe para cumprir a exigência dos [Termos de Serviço dos
Serviços de API do YouTube][tos] e descreve exatamente o que o programa faz
com dados.

## 1. Quem trata os dados

O próprio usuário, no computador dele. Quem instala e executa o Veo+ é o
controlador dos dados que o programa manipula. A Vecola Productions não
recebe, não armazena e não tem acesso a esses dados.

## 2. Que dados o programa acessa

**Do YouTube, por meio da API, apenas do canal que o usuário autorizou:**

| Dado | Para quê | Onde fica |
|---|---|---|
| Token de acesso e de renovação (OAuth) | Autorizar o envio do vídeo e da miniatura | Arquivo local na pasta do perfil (`perfis/<perfil>/credenciais/youtube/`) |
| Nome, foto e identificador do canal | Mostrar na interface para qual canal o vídeo vai | Arquivo local na pasta do perfil |
| Identificador e endereço do vídeo enviado | Histórico de envios do perfil | Arquivo local na pasta do perfil |

**Do computador do usuário:** a amostra de voz que ele mesmo fornece, os temas
que ele digita, os roteiros, áudios, cenas e vídeos produzidos.

O programa **não** acessa canais de terceiros, não lê comentários, não lê
métricas, não gerencia inscrições e não altera configurações do canal. Ele só
envia o vídeo e a miniatura que o usuário mandou enviar.

## 3. Escopos de autorização solicitados

| Escopo | Por que é necessário |
|---|---|
| `youtube.upload` | Enviar o arquivo de vídeo e a miniatura |
| `youtube.readonly` | Ler o nome e a foto do canal autorizado, para identificá-lo na interface |

Escopos mais amplos, como `youtube` e `youtube.force-ssl`, **não** são
pedidos.

## 4. Onde os dados ficam e por quanto tempo

Tudo em disco local, na pasta de trabalho do Veo+ (por padrão
`%LOCALAPPDATA%\Veo+\canal`, ou outra pasta escolhida pelo usuário). Cada
perfil de canal guarda o próprio token separado, para que um perfil nunca envie
para o canal de outro.

Os dados permanecem até o usuário apagá-los. Não há cópia remota, backup em
nuvem nem telemetria. Desinstalar o programa não apaga essa pasta, para não
destruir projetos do usuário; ela pode ser apagada manualmente.

## 5. Com quem os dados são compartilhados

A Vecola Productions não recebe dado algum. As requisições de rede que o
programa faz são:

- para a **API do YouTube**, com o token do próprio usuário, para enviar o
  vídeo e a miniatura e ler o nome e a foto do canal;
- para o **assistente de IA que o próprio usuário instalou e conectou à conta
  dele** (Claude Code, da Anthropic, ou Codex, da OpenAI), que recebe o tema e
  os textos do roteiro para escrevê-lo e revisá-lo. Esse envio segue a conta e
  a política de privacidade do provedor escolhido pelo usuário. **Nenhum dado
  obtido da API do YouTube é enviado a esses assistentes;**
- para baixar, somente após confirmação do usuário, componentes de que o
  programa precisa (por exemplo, Python, modelos de voz e de transcrição).

A narração com a voz do usuário, a transcrição e a renderização 3D são feitas
localmente; a amostra de voz não sai do computador.

## 6. Como revogar o acesso

Pelo programa: **Configurações, Canal e publicação, Desconectar canal**. O
Veo+ revoga a permissão no Google e apaga o token do disco.

Pela conta Google, de forma independente do programa:
[myaccount.google.com/permissions](https://myaccount.google.com/permissions).

## 7. Dados de API do YouTube

Este programa usa os Serviços de API do YouTube. Ao usá-lo, o usuário
concorda com os [Termos de Serviço do YouTube][termos-yt] e fica sujeito à
[Política de Privacidade do Google][privacidade-google].

Dados obtidos da API do YouTube são usados apenas para as funções descritas
acima, ficam somente no computador do usuário e são removidos quando ele
desconecta o canal ou apaga a pasta do perfil.

## 8. Contato

Dúvidas e pedidos relacionados a dados: abra uma issue em
[github.com/Vecolas/veoplus-politica](https://github.com/Vecolas/veoplus-politica/issues).

© 2026 Vecola Productions. Todos os direitos reservados.

[tos]: https://developers.google.com/youtube/terms/api-services-terms-of-service
[termos-yt]: https://www.youtube.com/t/terms
[privacidade-google]: https://policies.google.com/privacy
