---
{"dg-publish":true,"permalink":"/SisVida/Back/APIs REST/"}
---

## Visão Geral

Uma **API REST (Representational State Transfer)** é um estilo de arquitetura para comunicação entre sistemas, geralmente via HTTP.  
É muito usada em Desenvolvimento Backend com [[SisVida/Back/Express\|Express]] e [[SisVida/Back/Node.js\|Node.js]].

---

## Principais Características

- Baseada em recursos (ex: `/users`, `/products`).
    
- Usa métodos HTTP
    
    - `GET` → ler dados
        
    - `POST` → criar dados
        
    - `PUT/PATCH` → atualizar dados
        
    - `DELETE` → remover dados
        
- Retorna dados em JSON ou XML (JSON é o mais comum).
    
- Stateless → cada requisição é independente.
    

---

## Casos de Uso

- Comunicação entre [[SisVida/Front/Front\|Front]] e [[SisVida/Back/Back\|Back]].
    
- APIs Públicas (ex: Google Maps API, Twitter API).
    
- Aplicações móveis e web que consomem dados do servidor.