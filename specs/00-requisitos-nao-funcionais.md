# Requisitos Não-Funcionais

# Stack Tecnológica

As seguintes tecnologias serão utilizadas:
- Frontend
    - HTML
    - CSS (opções de framework são Bulma e Tailwind)
    - Javascript (sem framework)

- Backend
    - Python utilizando FASTAPI, psycopg2

- Banco de dados
    - PostgreSQL com a connection string:
    postgresql://neondb_owner:<password>@ep-twilight-lab-acewge2c-pooler.sa-east-1.aws.neon.tech/neondb?sslmode=require&channel_binding=require

- Segurança
    - Todos os inputs devem ser protegidos contra vulnerabilidades como XSS scripting, SQL injection e outros tipos conhecidos de vulnerabilidades
    - a API deve ter seus endpoints de backend protegidos para não permitir acesso indevido
    - O único endpoint aberto deve ser o que permite a utilização da URL encurtada

- Arquitetura
    - A aplicação deve seguir o padrão mais simples possível, escrito como uma API que tem um endpoint que serve o frontend

