# BarberHub

Sistema de agendamento online da **DS Barbearia**, feito com Python e Django.

O cliente marca o próprio horário pelo celular, escolhendo barbeiro, serviço e um horário livre. Os barbeiros veem a agenda do dia em um painel.

> 🚧 Projeto em desenvolvimento.

## Tecnologias

- Python 3.13
- Django 5.2 LTS
- SQLite
- Bootstrap

## Como rodar localmente (Windows)

1. Clone o repositório e entre na pasta:
   ```powershell
   git clone https://github.com/yvinsan/barberhub.git
   cd barberhub
   ```
2. Crie e ative o ambiente virtual:
   ```powershell
   py -3.13 -m venv .venv
   .venv\Scripts\Activate.ps1
   ```
3. Instale as dependências:
   ```powershell
   pip install -r requirements.txt
   ```
4. Copie o arquivo `.env.example` para `.env` e gere uma chave secreta:
   ```powershell
   copy .env.example .env
   python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"
   ```
   Cole a chave gerada no `.env`, no lugar de `gere-uma-chave-nova-aqui`.
5. Crie o banco de dados e rode o servidor:
   ```powershell
   python manage.py migrate
   python manage.py runserver
   ```
6. Acesse http://127.0.0.1:8000

## Autor

Yvin Oliveira — estudante de Engenharia de Software (UVA)