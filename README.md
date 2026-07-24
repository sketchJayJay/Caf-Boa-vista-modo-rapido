# Café Boa Vista — Automação Máxima

Versão separada do sistema, criada para reduzir digitação e trabalho repetitivo no balcão.

## Principais automações

- Ao selecionar o cliente, carrega automaticamente:
  - sacas em depósito;
  - vendas a pagar;
  - valores que o cliente pegou;
  - juros atualizados;
  - líquido do acerto;
  - última prova;
  - Pix/conta principal.
- Prova pode virar café em depósito no mesmo salvamento.
- Venda parcial:
  - confere saldo;
  - baixa o lote;
  - registra histórico;
  - cria financeiro;
  - gera recibo;
  - prepara WhatsApp.
- Acerto automático:
  - vendas menos valores pegos e juros;
  - cria backup antes de confirmar;
  - fecha vendas e desconta adiantamentos;
  - registra somente o líquido pago.
- Tela de pendências automáticas.
- Fechamento diário pronto para imprimir ou enviar.
- Backup automático diário e também depois de cada alteração.
- Mantém os 30 backups automáticos mais recentes.

## Coolify

- Build Pack: `Dockerfile`
- Porta: `8080`
- Destination Path do volume: `/app/data`
- Use um Volume Name exclusivo para este novo link.

## Variáveis

```env
PORT=8080
PYTHONUNBUFFERED=1
TZ=America/Sao_Paulo
SECRET_KEY=troque-por-uma-chave-grande-e-secreta
DATA_DIR=/app/data
```

## Importante

Não inclua banco de dados dentro do ZIP. Os dados devem permanecer no volume `/app/data`.
