# Nextos 5.1 Hyper — r188

UID **20261110074749** · Linux **5.15.223** · AArch64.

Uma imagem para os perfis suportados. A imagem de fábrica é distribuída sem jogos ou coleções.

## Novidades

- Atualização: o acompanhamento continua funcionando quando o sistema demora a responder, evitando o aviso falso de que a atualização foi interrompida.
- Atualização: a checagem automática ao abrir o menu é pulada quando uma atualização ainda está terminando, evitando o aviso de espera nessa hora.
- TV antiga sem imagem: nos aparelhos GXL, a ROM escolhe RGB quando a TV não declara YCbCr 4:4:4 ou quando a identificação da TV falha; TVs que declaram esse formato continuam usando a mesma cor de antes.
- Vídeo: quando a TV não declara o modo preferido do menu, a ROM tenta outra resolução compatível. Se a troca falhar, tenta voltar ao modo anterior, sem impedir a abertura do menu.
- TV antiga sem imagem: opção COR HDMI para escolher Automático, RGB ou YCbCr 4:4:4. Se não conseguir ver o menu, crie hdmi-rgb.txt na raiz da partição BOOT do cartão ou peça ao suporte para ativar RGB.
- Vídeo: corrigido nos aparelhos GXL o uso do escalador de imagem que podia deixar a tela preta ou o logo de fábrica por cima do menu após trocar a resolução. A troca por jogo usa a saída real, mantém o escalador ativo e restaura a janela do menu ao sair.
- Informações e diagnóstico: mostram a resolução e a cor reais da saída HDMI e o motivo da escolha (por exemplo, RGB porque a TV não declara YCbCr 4:4:4).
- Cartão novo: a resolução de fábrica do menu passa a ser 720p, a mesma que o menu já usava; quem atualiza mantém a configuração que tem.
- DOS e ScummVM: a música MIDI sai pelo GeneralUser já configurado, sem precisar escolher nada; MT-32 fica disponível colocando os ROMs MT-32 em roms/bios. Escolhas já feitas pelo jogador são mantidas.
- Diagnóstico: mostra se o Wi-Fi do aparelho aceita WPA3, chip por chip; redes mistas WPA2/WPA3 continuam funcionando como antes.

## Atualização e compatibilidade

Atualização física r187 → r188 confirmada no TX9 e no Aquário. O contrato permanece igual ao da r187: pacote nativo `flat25`, manifesto assinado, GitHub principal e R2 de reserva. BASE, versão residente, jogos, saves e configurações são preservados.

Clientes modernos (segunda r178 e posteriores) usam o atualizador do menu. As builds r170 até a primeira r178 recusam a OTA antes de tocar no BOOT e mantêm a rota manual pelo lançador do pacote, quando aplicável. Os contratos históricos foram conferidos no PC; isso não representa teste físico de todas essas versões. OLD 5.0/3.14 e o suporte por código permanecem intactos.

### Aviso de acompanhamento em instalações r187

Na atualização da r187 para a r188, o aviso de acompanhamento ainda pode aparecer uma vez. Se a tela de atualização mostrar erro de acompanhamento, normalmente a atualização já ficou preparada: reinicie pelo menu e confira a versão em Informações; só repita se continuar a versão anterior.

## Escopo da validação

A prova física desta entrega cobre TX9 e Aquário. Os casos de TV antiga (só RGB, DVI, sem EDID e EDID sem 720p) e hdmi-rgb.txt foram conferidos no PC com o script real sobre sysfs simulado. No TX9, com o monitor da casa, foram validados RGB forçado, automático e troca por jogo; as provas anteriores dos componentes preservados foram reaproveitadas.

A música MIDI foi provada no aparelho com DOSBox SDL2 e Doom em General MIDI. ScummVM e o core padrão dosbox_pure foram conferidos no PC e na configuração instalada. MT-32 não foi testado por falta dos ROMs, que devem ser fornecidos pelo jogador. Os demais perfis mantêm seus DTBs e a compatibilidade já existente. O Moonlight mantém o componente já validado na r187, cuja prova transmitiu a área de trabalho do PC; não houve nova sessão de streaming na r188. No Aquário, H.264 usa hardware e HEVC segue em software. Os caminhos e as configurações atuais de VMU do Flycast são preservados; o A1 por jogo não é mesclado com o A1 compartilhado de outro emulador.

## Integridade

| Arquivo | Bytes | SHA-256 |
|---|---:|---|
| `Nextos-5.1-20261110074749.img.gz` | 1809661517 | `38cd80c6b23220a271b93f75f1e774163990719632d4f0c025ded0d47f9566c7` |
| `Nextos-5.1-20261110074749-update.zip` | 1804394787 | `7c2cffcab4314f915971e15783c027c76c016f0f22b3aa02ceccdde69b3cb9b4` |

SYSTEM: `e5b5ac3e0aefc869e2f38cc9c25efaab3543d5d00e1c4c4d9941d73709043016`. Fonte compilada: `476184464b074a61a5d4493e005825bcf1219bcd`.

Confira `SHA256SUMS`, `SHA256SUMS.sig` e a chave pública de confiança. Os arquivos automáticos “Source code” do GitHub contêm apenas a documentação de distribuição e não instalam a ROM.
