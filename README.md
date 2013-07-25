opencart-cielo-extension
========================

A Cielo extension integration for Open Cart

Informações:
************

- Módulo para integração com Cielo.
- O módulo tem suporte ao cartão de débito Visa Electron, e cartões de crédito Visa, MasterCard, Dinners, Discover e Elo.
- O módulo permite o parcelamento pela loja ou pela administradora.
- O módulo possui uma página personalizada para informar o cliente que o pedido não foi aprovado.
- O módulo registra no histórico do pedido o Nº do Pedido, TID, Cartão e Parcelas.
- Para utilizá-lo é necessário ter contrato com a Cielo.

Versão:
*******

- 1.1

Compatibilidade:
****************

- OpenCart 1.5.1.3, 1.5.2.1 e 1.5.3.1

Instruções:
***********

- Execute o conteúdo do arquivo sql.txt via gerenciador do seu banco de dados para
  que seja criada a tabela onde ficará armazenado os dados do XML de retorno da Cielo.

- Após a criação da tabela, copie as pastas e arquivos para o raiz da instalação do 
  OpenCart. Acesse a administração da loja para habilitá-lo em Formas de Pagamento.

- Afiliação: Solicite a Cielo seu código de afiliação.

- Chave: Solicite a cielo uma chave de teste.

- Operação: Modo de Teste (Sim).

- Cartões para teste:

  Cartão com autenticação: 4012001037141112 (visa)
  Cartão sem autenticação: 4012001038443335 (visa), 
                           5453010000066167 (mastercard), 
                           6362970000457013 (elo), 
                           36490102462661 (diners),
                           6011020000245045 (discover).
  Data de validade: qualquer uma posterior ao mês e ano corrente.
  Código de segurança: qualquer número no total de 3 casas decimais.
  Valor do pedido: para simular uma transação autorizada, use qualquer valor em que os
                   dois últimos dígitos sejam zeros, senão toda autorização será negada.

Atenção:
********

- Este módulo é oferecido sem qualquer garantia ou suporte.
- O ambiente de testes da Cielo é extremamente lento e por muitas vezes não reponde, por isso
  preferencialmente teste após as 19:00 hs até as 6:00 hs. Já o ambiente de produção não tem
  esse problema de lentidão e não reponder.
- Faça primeiro os testes com o módulo em "Modo de Teste", após tudo funcionar sem problemas
  no "Modo de Teste", então mude suas configurações do módulo para "Modo de Teste (Não)",
  e coloque a nova chave que não deve ser mais a "chave de teste" e sim a "chave de produção",
  para que se dê inicío ao processo de homologação.

Homologação:
************

O objetivo dessa fase é assegurar que a integração esteja funcionando de maneira adequada. Ela
é iniciada após o término da implementação. Após a integração da loja feita com o ambiente de
Teste (da Cielo). É composta pelas seguintes etapas:

1) Finalização do cadastro junto à Cielo e recebimento da chave de produção
2) Execução de testes na loja virtual integrada ao ambiente de produção da Cielo
3) Homologação pela Cielo

Na primeira etapa, o lojista solicita a chave de produção. Para tanto é necessário enviar para
cieloecommerce@cielo.com.br as seguintes informações (que irão completar o cadastro):

- URL definitiva do site (ambiente de produção)
- Nome da empresa responsável pelo desenvolvimento da integração
- Nome e e-mail do técnico (desenvolvedor) responsável pela integração
- Número de afiliação (junto a Cielo) da loja virtual
- Razão social e nome fantasia da loja virtual
- URL do logotipo da loja, no formato GIF e tamanho de 112X25 pixels
- Usuário e senha na loja virtual para efetuar compras

Em resposta, a Cielo retorna uma chave válida no ambiente de produção. Logo a loja está
habilitada a realizar seus testes nesse ambiente. Inicia-se a segunda etapa. É importante que
testes sejam realizados para cobrir os seguintes tópicos:

 - Interação com os Web Services: testes com todas as funcionalidades utilizadas
 - Integração visual: a ida e a volta do fluxo a Cielo (os fluxos alternativos devem ser considerados)
 - Aplicação correta da marca da bandeira
 - Modalidades de pagamento: testes com as combinações possíveis de pagamento

Ao término, uma nova solicitação deve ser enviada para cieloecommerce@cielo.com.br, para que
a Cielo realize a homologação de fato. Um conjunto de testes então é executado. Para aprovar e
negar transações. O resultado, homologado ou não-homologado, é enviado por e-mail.

Desenvolvedores:
****************
- Pedro (Micropoint);
- Manoel Vidal (Comunidade OpenCart Brasil)
- Vários membros da comunidade OpenCart Brasil.

Agradecimentos:
***************
- Deus;

Aproveite!