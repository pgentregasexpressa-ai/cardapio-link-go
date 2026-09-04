# Cardápio Digital LinkGo

MVP de cardápio digital com Next.js + Supabase + WhatsApp, preparado para Vercel.

## 1. Instalar

```bash
npm install
npm run dev
```

## 2. Supabase

1. Crie um projeto no Supabase.
2. Abra SQL Editor.
3. Execute `supabase/schema.sql`.
4. Crie um usuário em Authentication > Users.
5. Insira um restaurante em `restaurants` usando o `id` do usuário em `owner_id`.

Exemplo:

```sql
insert into restaurants (owner_id, name, slug, whatsapp)
values ('UUID_DO_USUARIO', 'Meu Restaurante', 'meu-restaurante', '5542984168671');
```

## 3. Variáveis

Copie `.env.example` para `.env.local` e preencha:

```env
NEXT_PUBLIC_SUPABASE_URL=...
NEXT_PUBLIC_SUPABASE_ANON_KEY=...
NEXT_PUBLIC_RESTAURANT_SLUG=meu-restaurante
NEXT_PUBLIC_WHATSAPP=5542984168671
```

## 4. GitHub

```bash
git init
git add .
git commit -m "MVP cardapio digital"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/cardapio-linkgo.git
git push -u origin main
```

## 5. Vercel

Importe o repositório no Vercel e cadastre as mesmas variáveis de ambiente.

O MVP abre o pedido no WhatsApp com a mensagem pronta. O número padrão é +55 42 98416-8671.

## Próximos módulos

- CRUD completo de categorias
- edição de produtos
- upload de imagens no Supabase Storage
- adicionais no produto
- painel de pedidos
- horários de funcionamento
- múltiplos restaurantes por slug
- integração futura com a API da LinkGo
