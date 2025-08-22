---
{"dg-publish":true,"permalink":"/SisVida/Back/WebSockets/"}
---

## Visão Geral

[[SisVida/Back/WebSockets\|WebSockets]] é um protocolo que permite **comunicação bidirecional em tempo real** entre cliente e servidor.  
Diferente de HTTP, a conexão permanece aberta.

---

## Principais Características

- Comunicação **em tempo real**.
    
- Conexão persistente → não é necessário abrir/fechar a cada requisição.
    
- Baixa latência → ideal para interações rápidas.
    
- Suporte em [[SisVida/Back/Node.js\|Node.js]] através de bibliotecas como `ws` ou frameworks como Socket.IO.