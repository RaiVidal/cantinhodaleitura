# Cantinho da Leitura

Biblioteca digital para descobrir livros, ler PDFs e ouvir audiolivros. O projeto reúne um acervo público, uma área pessoal de leitura e um painel para gerenciar os materiais da biblioteca.

## Funcionalidades

- Catálogo público com busca e filtros por categoria e formato
- Leitor de PDF e reprodutor de audiolivros
- Favoritos, listas de leitura, histórico e marcadores de página
- Painel administrativo para cadastrar livros, capas, categorias e arquivos

## Tecnologias

Ruby 3.4.13 · Rails 8.1 · PostgreSQL · Vue 3 · Vite 8 · PDF.js

## Como executar

Tenha Ruby 3.4.13, Node.js 26.13.0 e PostgreSQL instalados. Clone o repositório e instale as dependências na raiz do projeto.

```sh
git clone https://github.com/RaiVidal/cantinhodaleitura.git
cd cantinhodaleitura
bundle install
npm ci
```

Configure a conexão com o PostgreSQL no ambiente local. O Rails usa `127.0.0.1:5432`, o usuário `postgres` e o banco `cantinhodaleitura_development` por padrão. Use `DATABASE_HOST`, `DATABASE_PORT`, `DATABASE_USERNAME`, `DATABASE_PASSWORD` e `DATABASE_NAME` para ajustar a conexão.

```sh
bundle exec rails db:prepare
```

Em terminais separados, inicie o Rails e o Vite.

```sh
bundle exec rails server
```

```sh
bundle exec vite dev
```

Abra o [acervo público local](http://localhost:3000/#/acervo-publico).

## Dados do acervo

A instalação começa com o acervo vazio. O cadastro de materiais é feito pelo painel administrativo com uma conta de administrador. O PostgreSQL guarda os cadastros e o Active Storage guarda as capas, os PDFs e os áudios em `storage/` no ambiente de desenvolvimento.


