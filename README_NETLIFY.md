# Auditoria para Netlify

Pasta pronta para upload manual no Netlify: publique o conteudo desta pasta, nao apenas o HTML.

## Corrigido nesta versao

- O arquivo principal esta como `index.html`.
- Os dois logos estao em `assets/` e os caminhos foram atualizados.
- Foram adicionados `meta description`, favicon, Open Graph basico e `netlify.toml`.
- O catalogo foi refeito a partir da planilha oficial `Tabela de Servicos e Precos - Solo e Companhia V2.xlsx`.
- O HTML agora possui os 50 servicos oficiais da planilha.
- Foi incluido o servico adicional `Sugestao de Adubacao e Calagem`, R$ 100,00, valido ate 5 amostras, com 1 sugestao por cultura.
- A base `sellerCouponDatabase` foi preparada para cupons por vendedor, mas comecou vazia e sem cupons ativos.
- O formulario foi adaptado para Netlify Forms com `multipart/form-data`, incluindo envio de anexo, dados do produtor, sacola de analises e totais.
- O envio do formulario usa POST nativo para a Netlify e deixa a confirmacao padrao da Netlify assumir o retorno.
- Foi incluido um formulario oculto de deteccao para garantir que o Netlify Forms registre `solicitacao-amostras` durante o deploy.
- O anexo e limitado no navegador a 1 arquivo de ate 8 MB, conforme suporte de upload do Netlify Forms.
- Os precos do catalogo e dos cards destacados foram alinhados aos valores oficiais.
- O antigo combo nao oficial foi substituido por `BioAS Max Plus`, servico existente na planilha.

## Ainda fora de escopo tecnico

- O envio por Netlify Forms so funciona quando o site estiver publicado na Netlify com deteccao de formularios habilitada. Em `file://` ou `localhost`, a pagina apenas valida os dados e mostra aviso de pre-visualizacao local.
- Se o envio publicado cair em 404, confira no painel da Netlify se o formulario `solicitacao-amostras` aparece em Forms e se o deploy ativo foi gerado a partir da branch `main`.
- Os cupons ainda rodam no navegador. Para validacao comercial segura, use backend ou Netlify Functions.
- A pagina depende de CDNs externos: Tailwind, Google Fonts, Lucide e html2pdf.
