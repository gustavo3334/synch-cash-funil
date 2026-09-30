# Synch Cash — funil de vendas

Funil estático com diagnóstico de 7 perguntas, captura do produto, vídeo e oferta. Publique a raiz deste repositório em uma hospedagem de sites estáticos; não há etapa de build. Mantenha `index.html` e os arquivos de mídia na mesma pasta.

## Checkout e mensuração

Os botões de compra levam ao checkout Cakto configurado no HTML. A oferta exibida é R$ 19,90 em pagamento único e o checkout pode acrescentar taxa de serviço. A Cakto deve confirmar o total e as condições antes da compra.

O navegador emite `synch_funnel_event` no `dataLayer` para `page_view`, `quiz_start`, `question_complete`, `diagnosis_complete`, `offer_view` e `checkout_click`. Configure o Pixel/Conversions API com o identificador da conta de anúncios e o evento de compra confirmado na Cakto; o HTML não confirma pagamentos. Nenhuma alternativa escolhida ou dado financeiro é enviada por esses eventos.
