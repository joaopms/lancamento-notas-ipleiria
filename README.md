# Lançamento de notas IPLeiria

Script em Python que permite verificar se houve alterações na Unidade Curricular na plataforma eLearning do IPLeiria.

## Preparando o Script

Para correr o script necessita de um sistema com Python instalado.

### Pre requisitos

Necessita de um sistema com Python configurado. Testado em Python 2.7-3.5. Necessita dos módulos requests e twilio instalados. Para configurar corra o seguinte comando.

```
python -m pip install requests twilio
```

É também necessário uma conta no serviço Twilio, que será usado para enviar os SMS.

### Configurando os seus dados

Necessita de editar o script Python e alterar as variáveis com o seu username e password.

```
USERNAME = "2171234"
PASSWORD = "qwerty"
TWILIO_SID = "ACXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
TWILIO_TOKEN = "your_auth_token"
TWILIO_TO_NUMBER = "+351987654321"
TWILIO_FROM_NUMBER = "+15017250604"
WAITING = 10
```

Ao alterar a variável **WAITING**, altera o intervalo de tempo de verificação à plataforma.

As variáveis **TWILIO_SID** e **TWILIO_TOKEN** correspondem aos dados de acesso à API do Twilio e as variáveis **TWILIO_TO_NUMBER** e **TWILIO_FROM_NUMBER** correspondem ao número de telemóvel para onde será enviada a mensagem SMS e o número de telemóvel de onde será enviada a mensagem SMS, respetivamente.

### Configurar as suas Unidades Curriculares

Para alterar quais as UCS deseja verificar, basta alterar a variável **UCS** e adicionar uma linha por UC, em que *uc* corresponde ao nome da cadeira e *url* ao link da UC na plataforma eLearning.

```
UCS = [
        {'uc':'SO','url':'https://ead.ipleiria.pt/2017-18/course/view.php?id=3659'},
        {'uc':'P2','url':'https://ead.ipleiria.pt/2017-18/course/view.php?id=3711'},
      ]
```

## Autores

* **Ruben Nogueira** - [rubnogueira](https://github.com/rubnogueira)
* **João Silva** - [joaopms](https://github.com/joaopms)