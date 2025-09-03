# TourTracker🎸
Aplicação para web scraping de shows com notificação automática por e-mail.

## 📌 Descrição
O TourTracker é um projeto em Python que realiza web scraping de uma página de tours utilizando Selectorlib.

Os dados extraídos são armazenados em um banco SQLite, e, sempre que um novo evento é detectado, o sistema envia uma notificação por e-mail.

O envio é feito via SMTP, com variáveis de ambiente protegidas pelo dotenv.

## Funcionalidades
- Extrair shows de uma página de tours
- Armazenar dados em banco SQLite
- Evitar duplicatas, verificando se o evento já existe
- Notificar novos shows encontrados via e-mail

## 🛠️ Tecnologias Utilizadas
- **Python** – linguagem principal
- **Requests** – captura do conteúdo da página
- **Selectorlib** – extração de dados via YAML
- **SQLite** – banco de dados local
- **smtplib + ssl** – envio de e-mails
- **dotenv** – gerenciamento de variáveis de ambiente

## 📚 Aprendizados
O desenvolvimento do TourTracker foi de suma importância pra que eu praticasse:

- Web scraping com requests e Selectorlib
- Integração com banco de dados SQLite
- Envio de e-mails com SMTP
- Uso de dotenv para proteger credenciais
- Estruturação de projetos Python reutilizáveis

## ▶️ Como Rodar Localmente
Clone o repositório:

``` bash
git clone https://github.com/gabriel-oligom/tour-tracker-scraping
cd tour-tracker-scraping
```

Crie e ative um ambiente virtual:
``` bash
python -m venv venv
source venv/bin/activate   # Linux / Mac
venv\Scripts\activate      # Windows
```

Instale as dependências:
``` bash
pip install -r requirements.txt
```

Configure as variáveis de ambiente no arquivo .env:
``` bash
EMAIL_USER=seu_email@gmail.com
EMAIL_PASSWORD=sua_senha
EMAIL_RECEIVER=destinatario@gmail.com
```

Execute a aplicação:
``` bash
# Windows
py main.py
# ou 
python main.py

# Linux / Mac
python main.py
```