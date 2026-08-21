# Dommo Sync

Canal público oficial de download do agente de captura de mãos da **DOMMO
Poker Team**.

O projeto, o backend e o código-fonte são privados. Este repositório público
contém somente esta documentação e os instaladores compilados anexados em
[Releases](../../releases).

## Instalar

1. Entre na [área de captura do site Dommo](https://system.dommopokerteam.com/player/captura).
2. Crie uma credencial para o computador e copie o valor exibido.
3. Baixe a versão estável mais recente:
   [DommoSyncSetup.exe](../../releases/latest/download/DommoSyncSetup.exe).
4. Abra o instalador e cole a credencial quando solicitado.

O assistente valida a credencial e configura o Dommo Sync para iniciar com o
Windows. A credencial válida libera o capturador próprio do Dommo; não é
necessário instalar o Asian Hand Converter. O jogador pode usar múltiplas contas
e mesas normalmente, com captura isolada por processo e sincronização em segundo
plano.

## Segurança

- nenhuma credencial é embutida no instalador público;
- o valor é protegido pelo DPAPI para o usuário atual do Windows;
- uma credencial pode ser revogada a qualquer momento no site;
- cada release informa o SHA-256 do instalador para conferência.

Compatível com Windows 10/11 x64.

## Atualizações

A partir da versão 0.7.0, o próprio Dommo Sync avisa quando existe uma versão
estável nova. O jogador pode baixar e iniciar a atualização pelo painel ou pelo
ícone perto do relógio; o app confere o SHA-256 publicado no release antes de
abrir o instalador.

Quem ainda usa a versão 0.6.0 ou anterior precisa instalar a 0.7.0 manualmente
uma última vez. Depois disso, os próximos avisos e downloads acontecem dentro do
aplicativo.
