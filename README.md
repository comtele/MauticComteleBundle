# Mautic Comtele Plugin

## Requisitos

- Testado no Mautic v2.15;
- PHP v7.0 ou superior.

## Instalação

```sh
$ cd plugins

$ git clone https://github.com/thalesamaria/MauticComteleBundle.git
```

Limpe o cache rodando os seguintes comandos na pasta raíz do seu Mautic:
```sh
$ php app/console cache:clear
```
```sh
$ php app/console cache:warmup
```
O comando abaixo reflete a maioria das instalações do Mautic no **Debian/Ubuntu utilizando Apache ou NGINX**:
```sh
$ chown -R www-data:www-data .
```
```sh
$ chmod -R g+rw .
```
```sh
php app/console mautic:assets:generate
```
```sh
php app/console mautic:plugins:reload
```
## Configuração
- Acesse a página de plugins pelo painel do Mautic e clique no botão **Instalar/Atualizar plugins**.
- Clique no Plugin Comtele, selecione publicado para SIM e insira sua chave de integração Comtele no campo Api Key.
- Salvar e fechar

### Chave Comtele
- Você encontra sua chave de integração acessando sua conta em https://sms.comtele.com.br.

## Como Usar
- No seu Mautic, acesse o menu Configuração;
  + Navegue até a aba Configuração de Mensagem de Texto e verifique se o transportador padrão está Comtele SMS;
- Criando Mensagem de Texto;
  + Para criar um modelo de mensagem, acesse Canais > Mensagem de Texto;
  + Exemplo: {contactfield=firstname}, testando o envio de SMS.
- Configurando a campanha:
  + Adicione uma nova ação;
  + Enviar Mensagem de texto;
  + Selecione a mensagem que deseja enviar.
  
### Observações
- O número do contato deve estar cadastrado no campo phone ou mobile;
- Caso os campo phone e mobile estejam preenchido, será considerado o campo phone;

## Dúvidas
- atendimento@comtele.com.br
- 0800 266 8353
- WhatsApp: (16) 98130-4898
