---
{"dg-publish":true,"permalink":"/SisVida/Back/Mongoose Schema/"}
---

## Visão Geral

O **[[SisVida/Back/Mongoose Schema\|Mongoose Schema]]** define a **estrutura dos documentos** em uma coleção do [[SisVida/Back/MongoDB\|MongoDB]].

---

## Principais Características

- Define os **campos** (ex: `username`, `password`).
    
- Permite definir **tipos de dados** (String, Number, Date, Boolean, etc.).
    
- Pode incluir **validações** (obrigatório, único, tamanho mínimo/máximo).
    
- Serve como base para criar um [[Mongoose Model\|Mongoose Model]].

```
const userSchema = new mongoose.Schema({
  username: { type: String, unique: true, required: true },
  password: { type: String, required: true }
});

```