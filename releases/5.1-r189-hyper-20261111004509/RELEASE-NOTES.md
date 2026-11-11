# Nextos 5.1 Hyper — r189

Atualize pelo menu **ATUALIZAÇÕES & TRANSFERÊNCIAS → ATUALIZAR RETRO ELITE**. A oferta escolhe o pacote compatível com a versão instalada. Para atualização manual, use **-unified-update.zip**.

## Correções e melhorias

- Preparo da inicialização sem recusa por espaço na BOOT, com recuperação preservada.
- Atualizações interrompidas e sobras do próprio atualizador são reconciliadas automaticamente. Os arquivos baixados são conferidos antes de aplicar.
- Depois da confirmação, pacotes, cópias temporárias e sistemas anteriores são removidos. Jogos, saves e configurações são preservados.
- Suporte automático com identidade individual vinculada ao aparelho e consentimento explícito. Use **AJUDA E SUPORTE → SUPORTE REMOTO → AUTORIZAR SUPORTE AUTOMÁTICO** para ativar. É possível revogar e autorizar novamente pelo menu.
- Atendimento por código independente do automático, com código na tela e prazo de até quatro horas.
- Aquário: retorno persistente ao cartão após a primeira entrada pelo aplicativo e melhorias de leitura do cartão e de inicialização.

## Validação e limites

Atualização pelo menu, saúde, limpeza, preservação de jogos e saves, abertura de jogo e os dois modos de suporte remoto aprovados no TX9 e no Aquário.

**Clientes r170–r188 precisam de 4 GiB livres no cartão para iniciar a atualização.** Libere espaço antes de tentar novamente, se necessário. A limpeza automática acontece depois que a versão nova é instalada.

No Aquário que nunca entrou pelo aplicativo, a primeira entrada continua pelo aplicativo **Reiniciar Retro Elite**. Depois disso, o início pelo cartão fica persistente. MODO SMART TV mantém o retorno ao Android. Não há formatação nem instalação no armazenamento interno do aparelho.

## Integridade

Os mestres e SHA256SUMS são assinados com Ed25519 pela chave pública NX. A imagem de fábrica é distribuída sem jogos. Os arquivos automáticos “Source code” do GitHub não instalam a ROM.

| Arquivo | Bytes | SHA-256 |
|---|---:|---|
| `Nextos-5.1-20261111004509-unified-update.zip` | 1562891092 | `6aa603549901f27238263963ccddc2f0f442ef392f1f1614a6d0cd4e3dc0d1f9` |
| `Nextos-5.1-20261111004509-update.zip` | 1526704905 | `b756f7ef40b5a38eb8cb9d60104a3f01594352c18f35fd8d677a54652c75850f` |
| `Nextos-5.1-20261111004509.img.gz` | 1568242533 | `4b0a97d5324a6658cbeef07c35600281c901e5c0c6c9c5045cce74258b817089` |

UID: `20261111004509`. SYSTEM: `d3474c63c24e589d5b229e1ba9f18359fe6fe74bf55361278a806498987d8c0a`.
