📖 [Documentação Postman](https://documenter.getpostman.com/view/33022213/2sA3XWdekL)
# authentication-django-api

Uma API de autenticação JWT com a funcionalidade "Esqueci minha senha". Este README fornece informações essenciais sobre como configurar e executar o projeto em seu ambiente local.

## Requisitos

Certifique-se de que você tenha os seguintes requisitos instalados em seu sistema:

- Python (versão recomendada: 3.7 ou superior)
- Django (instalado automaticamente ao seguir as instruções abaixo)
- Outras dependências listadas no arquivo `requirements.txt`


## Instalação das Dependências

Com o ambiente virtual ativado, instale as dependências do projeto usando o comando:
```bash
pip install -r requirements.txt
```


## Configuração de Email

No arquivo settings.py na pasta "app" do projeto, defina o email que irá enviar os emails com a solicitação de redefinir a senha aos usuários, juntamente com a senha do mesmo.
```bash
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'smtp.gmail.com' #Ou outro host
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = 'seuemail@host.com'
EMAIL_HOST_PASSWORD = 'suasenha'
DEFAULT_FROM_EMAIL = 'seuemail@host.com'
```


## Rodar o projeto

Após instalar as dependências, aplique as migrations no banco de dados com o comando:
```bash
python manage.py migrate
```

Agora o projeto jã pode ser inicializado com o comando:
```bash
python manage.py runserver
```

Após isso, o sistema estará pronto para ser acessado em:
[http://localhost:8000](http://localhost:8000)
