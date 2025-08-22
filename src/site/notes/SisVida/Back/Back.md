---
{"dg-publish":true,"permalink":"/SisVida/Back/Back/"}
---

# Backend Overview

Este backend foi construído usando [[SisVida/Back/Node.js\|Node.js]] com o framework [[SisVida/Back/Express\|Express]] e [[SisVida/Back/MongoDB\|MongoDB]] via [[SisVida/Back/Mongoose\|Mongoose]].  
Ele fornece um **sistema básico de autenticação de usuários** com endpoints para registro e login.

## Dependências

- **express** → Servidor HTTP e roteamento.
    
- **mongoose** → Conexão com o banco de dados e modelagem de schemas para [[SisVida/Back/MongoDB\|MongoDB]].
    
- **cors** → Habilita requisições cross-origin, permitindo integração com o frontend.
    
- **body-parser** → Faz o parsing de requisições JSON para acesso facilitado.
    

---

## Banco de Dados

- Conecta a uma instância local chamada `TCC_SUS`.
    
- Pode ser facilmente atualizado para conectar ao [[SisVida/Back/MongoDB\|MongoDB]].
    

---

## Modelo de Usuário

- Definido com [[SisVida/Back/Mongoose Schema\|Mongoose Schema]]:
    
    - `username` → Deve ser único.
        
    - `password` → Armazenado em texto puro (⚠️ sem criptografia ainda).
        
- Exposto como um modelo `User` para operações no banco de dados.
    

---

## Rotas da API

- **POST /register**
    
    - Entrada: `username`, `password`
        
    - Verifica se ambos foram fornecidos.
        
    - Valida a exclusividade do `username`.
        
    - Retornos:
        
        - `201 Created` → usuário registrado
            
        - `409 Conflict` → nome de usuário já existe
            
- **POST /login**
    
    - Entrada: `username`, `password`
        
    - Valida as credenciais no banco de dados.
        
    - Retornos:
        
        - `200 OK` → login bem-sucedido
            
        - `401 Unauthorized` → credenciais inválidas
            

---

## Inicialização do Servidor

- Roda na porta `3001`.
    
- Exibe uma mensagem de confirmação ao iniciar.
    

---

## Limitações e Questões de Segurança

- Senhas são armazenadas em **texto puro** (⚠️ inseguro).
    
- Não possui Hash de Senha com bcrypt.
    
- Não possui Autenticação JWT ou gerenciamento de sessões.
    
- Adequado apenas para **protótipo**, mas não seguro para Sistemas em Produção.