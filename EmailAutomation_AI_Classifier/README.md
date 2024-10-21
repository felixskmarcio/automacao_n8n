# Planejamento do Projeto - Classificação Inteligente de E-mails com OpenAI

felixBR  
Rua E, 20  
Penedo, AL, 57200-000  
+55 (82) 9.9827-4851  

## classificação inteligente de e-mails com OpenAI  
**19 de outubro de 2024**  

### Descrição do projeto
Este projeto visa automatizar o processo de classificação de e-mails recebidos em uma conta gmail, utilizando a plataforma n8n para a gestão dos fluxos de automação e a API da openai para análise semântica e categorização dos e-mails com base em seu conteúdo. a solução propõe a criação de categorias como "financeiro", "trabalho", "tecnologia", entre outras, de forma que os e-mails sejam automaticamente rotulados de acordo com o seu teor, otimizando a organização da caixa de entrada e a produtividade do usuário.

### Objetivos
- Automatizar a classificação de e-mails: utilizar a API do openai para realizar a análise semântica do conteúdo de cada e-mail e classificá-los automaticamente em categorias predefinidas, como "financeiro", "trabalho", "tecnologia", entre outras.
- Aplicar rótulos automaticamente no gmail: desenvolver fluxos automatizados na plataforma n8n para aplicar rótulos correspondentes aos e-mails conforme as categorias identificadas pela análise da IA.
- Reduzir o tempo de gestão manual da caixa de entrada: minimizar o tempo que os usuários gastam organizando e-mails, permitindo uma gestão mais eficiente por meio de rótulos automáticos.
- Garantir a integração segura e eficaz com o gmail: configurar a autenticação oauth2 para garantir a comunicação segura entre o n8n e a conta de e-mail do gmail, permitindo o acesso controlado à caixa de entrada.

### Requisitos
- Conta gmail autenticada via oauth2 para permitir que o n8n monitore a caixa de entrada e aplique rótulos automaticamente.
- Conta na API do openai com acesso ao modelo gpt para análise de texto.
- integração entre o n8n e a API do openai para processar e classificar os e-mails.
- Criação de fluxos no n8n para monitoramento dos e-mails e aplicação de rótulos.

### Tecnologias utilizadas
- N8N: plataforma low-code para automação de fluxos.
- Openai: API para processamento de linguagem natural (nlp) e categorização.
- Gmail API: para autenticação segura e interação com a conta de e-mail do usuário.

### Desenvolvimento e implementação

#### Configuração do n8n
- **Gmail trigger**: este nó é configurado para monitorar a caixa de entrada do gmail e capturar novos e-mails à medida que são recebidos.
  - Frequência de verificação: a cada minuto.
  - Gatilho: recebimento de novos e-mails.

#### integração com openai
- **Modelo de chat openai**: o texto dos e-mails será enviado para análise semântica.
  - O modelo gpt será utilizado para entender o conteúdo e categorizar os e-mails.

#### Categorização de e-mails
- **Classificador de texto**: após o processamento, o openai retornará a categoria que melhor se encaixa no conteúdo do e-mail. as categorias definidas no sistema são:
  - fFinanceiro
  - Trabalho
  - Tecnologia
  - Educação
  - Compras
  - Certificações
  - Segurança
  - Faturas e Cobranças

#### Aplicação de rótulos no gmail
- O sistema automaticamente aplicará os rótulos correspondentes no gmail com base na categoria atribuída.

#### Exemplo de fluxos
1. Recebimento de um e-mail com a palavra "fatura" resultará na atribuição do rótulo "financeiro".
2. E-mails contendo palavras como "reunião" ou "relatório" receberão o rótulo "trabalho".

### Plano de testes
**Exportar o workflow json**: o arquivo classificação inteligente de e-mails com openai já foi criado em formato json (fornecido para download no link acima). você pode importar esse arquivo json diretamente na sua instância do n8n.

- **Baixar o arquivo json**: use o arquivo que você baixou.
- **Importar no n8n**:
  1. No n8n, clique no botão importar no painel de controle.
  2. Selecione o arquivo json.
  3. O workflow será automaticamente carregado e você poderá editá-lo se necessário.

#### Testes funcionais
- Envie alguns e-mails com conteúdos de diferentes categorias como "financeiro", "trabalho" e "tecnologia" para a conta gmail configurada.
- Verifique se os rótulos estão sendo aplicados corretamente a cada e-mail.

#### Testes de integração
- Certifique-se de que a comunicação entre o n8n e a API do openai está funcionando. o status das requisições pode ser monitorado na interface do n8n, e os erros aparecerão caso haja algum problema com a autenticação ou o processamento de e-mails.

#### Testes de desempenho
- Avalie o tempo de resposta ao receber e processar cada e-mail. para isso, envie um grande volume de e-mails e verifique se o tempo de processamento aumenta ou se há gargalos.

### Termo de entrega
- **Projeto**: classificação inteligente de e-mails com openai
- **Cliente**: felixBR
- **Data de entrega**: 19/10/2024
