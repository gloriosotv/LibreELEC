🛠️ Como gravar multitool.img no cartão SD ou pendrive (Linux)

Este tutorial mostra como gravar a imagem multitool.img em um cartão microSD ou pendrive para uso em TV Boxes compatíveis com LibreELEC.
⚠️ Aviso

Tenha certeza absoluta do dispositivo (ex: /dev/sdc) que você irá usar. O comando dd irá apagar tudo nele!
✅ Passo a passo
1. Baixe a imagem multitool

🔗 Clique aqui para baixar multitool.img
2. Descubra qual é seu dispositivo

Conecte o cartão SD ou pendrive e execute:

lsblk

Anote o caminho do dispositivo (ex: /dev/sdc). Não use partições como /dev/sdc1.
3. Grave a imagem no dispositivo

sudo dd if=multitool.img of=/dev/sdX bs=4M status=progress

Substitua /dev/sdX pelo nome correto do seu dispositivo, como /dev/sdc.
4. Garante que todos os dados sejam gravados

sync

Esse comando força a gravação de todos os dados em cache no dispositivo — evita corrupção.
5. Ejete o dispositivo com segurança

sudo eject /dev/sdc

Substitua /dev/sdc pelo caminho do seu dispositivo.
📥 Outras imagens úteis

    multitool.img

    LibreELEC-RK322X.arm-12.0-nightly-20250218-6a1e364-rk322x.img
