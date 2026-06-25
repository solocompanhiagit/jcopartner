# Auditoria para Netlify

Pasta pronta para upload manual no Netlify: publique o conteudo desta pasta, nao apenas o HTML.

## Corrigido nesta versao

- O arquivo principal esta como `index.html`.
- Os dois logos estao em `assets/` e os caminhos foram atualizados.
- Foram adicionados `meta description`, favicon, Open Graph basico e `netlify.toml`.
- O catalogo foi refeito a partir da planilha oficial `Tabela de Servicos e Precos - Solo e Companhia V2.xlsx`.
- O HTML agora possui os 50 servicos oficiais da planilha.
- Foi incluido o servico adicional `Sugestao de Adubacao e Calagem`, R$ 100,00, valido ate 5 amostras, com 1 sugestao por cultura.
- Foi incluido o cupom global `Teste10`, com 10% de desconto.
- Foram incluidos os servicos `Solo Max Plus + Fosforos`, `Completa + Nitrogenio`, `MAP`, `Super Simples`, `Super Fosfato Triplo` e `Analise Metagenomica (Microbiologica)`.
- A base `sellerCouponDatabase` segue preparada para cupons por vendedor.
- A area de proposta foi simplificada para gerar PDF localmente; nao ha envio por formulario nem upload de anexo no site.
- O usuario deve gerar o PDF e anexar/enviar manualmente pelo canal desejado.
- Os precos do catalogo e dos cards destacados foram alinhados aos valores oficiais.
- O antigo combo nao oficial foi substituido por `BioAS Max Plus`, servico existente na planilha.

## Ainda fora de escopo tecnico

- Os cupons ainda rodam no navegador. Para validacao comercial segura, use backend ou Netlify Functions.
- A pagina depende de CDNs externos: Tailwind, Google Fonts, Lucide e html2pdf.
