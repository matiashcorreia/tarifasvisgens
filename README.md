# 🚗 Corridas & Viagens — Escada

Sistema de busca de tarifas para grupos de motoristas de Escada/PE.

## 📁 Estrutura

```
├── index.html        → App público (busca de tarifas por grupo)
├── super_admin.html  → Painel super admin (somente administrador geral)
```

## 🔧 Tecnologias

- HTML + CSS + JavaScript puro (sem frameworks)
- [Supabase](https://supabase.com) como banco de dados e autenticação

## 🚀 Deploy

Hospedado na [Vercel](https://vercel.com) com deploy automático a cada push.

## 👥 Acesso

| Perfil | URL | Acesso |
|--------|-----|--------|
| Público | `/` | Aberto |
| Super Admin | `/super_admin.html` | Email + senha (Supabase Auth) |
| Admin do Grupo | `/[slug]/` | Email + senha do grupo |

## ⚙️ Variáveis de ambiente

As credenciais do Supabase estão diretamente no HTML (anon key — segura para uso público).

## 📦 Banco de dados

Tabelas no Supabase:
- `grupos` — grupos de motoristas
- `bairros` — rotas entre bairros por grupo
- `viagens` — viagens longas por grupo
- `perfis` — usuários e permissões
- `bairros_padrao` — tabela padrão copiada para novos grupos
- `viagens_padrao` — tabela padrão de viagens
