# PREMULTISF Avalia (v5 — versão final)

Next.js 14 + Tailwind + Recharts. Lê a planilha de respostas a cada 60 s (e no botão "Atualizar"). Acesso livre, sem senha.

## Variáveis de ambiente (opcionais)
- `SHEET_ID` / `SHEET_TAB`: planilha e aba lidas (padrão: as do projeto).

## Onde ajustar a matriz (`lib/model.ts`)
- `INDS` e `MAP`: indicadores e o texto de cada afirmativa do formulário que alimenta cada um.
- `READ`: faixas de leitura (4,50 / 3,50 / 2,50). `compute()`: média integrada, índices, sinais de alerta.
- `REGISTROS`: % de conformidade dos dados de registro [D] por indicador (ex.: `{ "6.2": 82 }`); entram com peso igual à percepção.
- `EXPECTED`: pessoas esperadas por público (taxa de resposta / confiabilidade).
- `NDAE_A_PARTIR_DE`: ciclo em que a pergunta do NDAE (5.2) passa a valer (padrão 2027; 2026 = 1º ciclo).
- `CYCLE_START_MONTH`: mês de início do ciclo (1 = ano civil).

## Privacidade
Nome, e-mail e data nunca são lidos. Não há link para a planilha nem tabela de respostas individuais.

## Entrega e acesso (resumo)
- Ver o painel não exige conta. Publicar mudanças exige acesso ao GitHub (arquivos) e à Vercel (publicação).
- Recomendado: contas institucionais (e-mail da ESP/SMS, com verificação em duas etapas) no GitHub e na Vercel; repositório e projeto ficam nelas, com pelo menos 2 responsáveis.
- Plano gratuito (Hobby): 1 usuário que publica; commits de outras pessoas em repositório privado são bloqueados. Para mais pessoas publicarem, use o plano Pro (convite em Team Settings → Members).
- Tirar do ar: Vercel → projeto → Settings → General → Delete Project. O código continua no GitHub e pode ser publicado de novo.
- Não deixe o repositório público: o ID da planilha está no código (lib/sheet.ts).
- Formulário e planilha: transfira a propriedade para a conta institucional e mantenha "Qualquer pessoa com o link" (Leitor) na planilha.
