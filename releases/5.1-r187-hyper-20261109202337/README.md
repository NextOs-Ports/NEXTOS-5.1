# Nextos 5.1 Hyper — r187

UID **20261109202337** · Linux **5.15.223** · AArch64.

Uma imagem para os perfis suportados. A imagem de fábrica é distribuída sem jogos ou coleções.

## Novidades

- Jogos abrem mais rápido: cerca de 1 a 2 segundos a menos do toque até o jogo aparecer, sem mudar nenhuma configuração.
- Desempenho: ao sair de um jogo, o processador volta ao modo normal do menu; antes ficava no máximo até reiniciar o menu ou o aparelho, esquentando à toa.
- Boot: o menu fica pronto mais cedo, com o cache dos componentes de vídeo já gerado na ROM e as pastas de jogos lidas em segundo plano durante a abertura.
- Jogar do PC: novo sistema Moonlight no menu. Pareie com o PC pelo PIN, veja a lista do que o PC oferece e abra no aparelho o que o PC oferece, com vídeo decodificado por hardware; SELECT+START encerra e volta ao menu.
- Vídeo: no Aquário (S905W2) os vídeos H.264 passam a ser decodificados por hardware, usando o firmware do próprio Android do aparelho; se não der, o vídeo continua tocando por software, sem aviso.
- N64: novo emulador opcional Mupen64Plus pow2, com desenho por software; escolha nas opções do sistema ou do jogo. O emulador padrão do N64 continua o mesmo.
- N64: com o pow2, os saves ficam na mesma pasta do Mupen64Plus atual, o som sai normalmente e SELECT+START fecha o jogo.
- N64: o pow2 pula quadros sozinho só quando o aparelho atrasa, para manter o jogo na velocidade certa; jogos muito pesados ainda podem ficar abaixo da velocidade cheia no TX9.
- PS1: o DuckStation Elite passa a funcionar também no Aquário (Mali-G31); o DuckStation de antes continua disponível, como na versão anterior.
- PSP: a opção escolhida para um jogo agora vale só para aquele jogo, e não para os próximos.
- PSP: pular quadros (frameskip) e sincronia vertical (vsync) aparecem no menu e passam a valer de verdade nos dois PPSSPP.
- PSP: corrigido o PPSSPP que recusava a GPU em aparelhos com Mali-G31; aparelhos com Mali-450 seguem iguais.
- Saves: os saves de PSP, NDS (DraStic e DSperate), ScummVM, N64, PS1 e 3DS passam a ficar também em roms/saves/<sistema>, junto com os do RetroArch; os arquivos originais são preservados e dá para voltar ao jeito anterior.
- Menu: com o menu parado ele quase não usa o processador e volta na hora ao primeiro toque; a rolagem continua suave.
- Menu: o menu ocupa menos memória enquanto você joga e na tela inicial, sobrando mais para o jogo.
- Menu: capas e imagens carregam mais rápido.
- Menu: lista de sistemas mais enxuta — 28 sistemas de hacks e variantes agora ficam dentro do console de origem, utilitários vão para Ferramentas e Switch, Vita e Xbox ficam em Exclusivos. Nenhum jogo foi movido ou apagado.
- Menu: o sistema "mastersystem MARK III" passa a se chamar markiii; as escolhas que você já tinha feito para ele são mantidas.
- Wi-Fi: várias redes salvas; o aparelho conecta sozinho na que estiver disponível, dá para esquecer uma rede sem perder as outras, e senhas com caracteres especiais funcionam.
- Som: se o servidor de som parar, ele volta sozinho em poucos segundos, com o volume preservado.
- Envio pelo navegador: mandar vários arquivos seguidos não dá mais o aviso falso de "Outro envio está em andamento".
- Memória: quando falta memória, o jogo é o primeiro a ser fechado e o motivo aparece na tela, em vez de o aparelho travar.
- Cores baixados: um core só é usado se tiver assinatura válida para a ROM instalada; um core não autorizado é ignorado e o jogo abre com o core de fábrica, com aviso uma vez.
- Dreamcast: no Flycast e no Flycast Dojo, a proporção de tela escolhida no menu passa a ser aplicada, só naquela sessão.
- Diagnóstico: mostra, por formato de vídeo, se a decodificação é feita por hardware e qual caminho está em uso.
- Diagnóstico: falhas graves do sistema ficam registradas no cartão, com tamanho limitado e sem dados pessoais, para o suporte, nos aparelhos que guardam esse registro entre reinícios.

## Atualização e compatibilidade

Atualização física r186 → r187 confirmada no TX9 e no Aquário. O contrato permanece igual ao da r186: pacote nativo `flat25`, manifesto assinado, GitHub principal e R2 de reserva. BASE, versão residente, jogos, saves e configurações são preservados.

Clientes modernos (segunda r178 e posteriores) usam o atualizador do menu. As builds r170 até a primeira r178 recusam a OTA antes de tocar no BOOT e mantêm a rota manual pelo lançador do pacote, quando aplicável. Os contratos históricos foram conferidos no PC; isso não representa teste físico de todas essas versões. OLD 5.0/3.14 e o suporte por código permanecem intactos.

### Aviso de acompanhamento em instalações r186

Se a tela de atualização mostrar erro de acompanhamento, normalmente a atualização já ficou preparada: reinicie pelo menu e confira a versão em Informações; só repita se continuar a versão anterior.

## Escopo da validação

A prova física desta entrega cobre TX9 e Aquário. Os demais perfis mantêm seus DTBs e a compatibilidade já existente. A prova do Moonlight transmitiu a área de trabalho do PC. No Aquário, H.264 usa hardware e HEVC segue em software. Os caminhos e as configurações atuais de VMU do Flycast são preservados; o A1 por jogo não é mesclado com o A1 compartilhado de outro emulador.

## Integridade

| Arquivo | Bytes | SHA-256 |
|---|---:|---|
| `Nextos-5.1-20261109202337.img.gz` | 1809644262 | `37a3551f3ac24fe76d34722dd601d7779e98afa12c79d7f4326ce06d776a7564` |
| `Nextos-5.1-20261109202337-update.zip` | 1804374615 | `904a05932955f9e2d6ac07527df88854a60eb44890cc37649c2fc08f55b1ec5b` |

SYSTEM: `3c56c4b50e02b107f43e2917aa74da0aef84fb277f889db18471e34768c84664`. Fonte compilada: `4b987228b4d8dcec7f47d616fb7379eba7ba2d8e`.

Confira `SHA256SUMS`, `SHA256SUMS.sig` e a chave pública de confiança. Os arquivos automáticos “Source code” do GitHub contêm apenas a documentação de distribuição e não instalam a ROM.
