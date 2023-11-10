# Tutorial de Instalação e Uso - Envio de E-mails com Matplotlib

Este tutorial fornece instruções passo a passo para instalar e utilizar a função de envio de e-mails com anexos de gráficos do Matplotlib em Python.

## Pré-requisitos

Certifique-se de ter o Python 3 instalado em seu sistema. Além disso, você precisará instalar as bibliotecas necessárias. Execute o seguinte comando no terminal para instalar as dependências:

```bash
pip install matplotlib io smtplib email python-dotenv
```

## Configuração

1. **Criar um arquivo `.env`**
   Crie um arquivo chamado `.env` no diretório do seu projeto. Adicione as seguintes linhas e substitua `SEU_EMAIL@gmail.com` e `SUA_SENHA` pelos dados da sua conta do Google:

  Siga as instruções em https://support.google.com/accounts/answer/185833?hl=pt para gerar a senha de aplicativo.

   ```env
   AUTH_EMAIL=SEU_EMAIL@gmail.com
   AUTH_PASS=SUA_SENHA
   ```
Certifique-se de manter este arquivo seguro e não compartilhe com outras pessoas.

## Exemplo de Uso

```python
# Exemplo de Uso
titulo = "Relatório Mensal"
mensagem = "Segue anexo o relatório mensal com os gráficos."
lista_de_imagens = [figura1, figura2]  # Substitua com suas figuras do Matplotlib
para = "destinatario@email.com"

envio_resultado(titulo, mensagem, lista_de_imagens, para)
```
Certifique-se de substituir destinatario@email.com pelo endereço de e-mail do destinatário real.
