# Dommo Sync

Agente que sincroniza automaticamente as mãos de poker capturadas pelo
**Asian Hand Converter** com o servidor de estudo do time.

Roda em segundo plano no PC do jogador, observa a pasta de hand histories e
envia as mãos novas conforme são geradas. Não modifica nada no seu jogo — apenas
lê os arquivos que o Asian já grava.

## Instalação

1. Baixe o `dommo-sync.exe` na aba [Releases](../../releases).
2. Crie um arquivo `run.bat` na mesma pasta com o conteúdo abaixo
   (peça ao admin do time o `SERVER_URL` e o seu `AUTH_TOKEN`):

```bat
@echo off
set WATCH_DIR=C:\Program Files (x86)\Ace Poker Solutions\Asian Hand Converter\HM3HandHistories\sprp_hh
set SERVER_URL=https://SEU-SERVIDOR
set AUTH_TOKEN=SEU-TOKEN
set STATE_FILE=%~dp0offsets.json
dommo-sync.exe
```

3. Dê duplo clique em `run.bat` (ou coloque no atalho de inicialização do Windows).

O agente faz uma varredura inicial dos arquivos existentes e depois envia cada
mão nova automaticamente.

## Configuração (variáveis de ambiente)

| Variável | Descrição |
|---|---|
| `WATCH_DIR` | Pasta `sprp_hh` do Asian Hand Converter |
| `SERVER_URL` | URL do servidor de ingestão do time |
| `AUTH_TOKEN` | Token individual do jogador |
| `STATE_FILE` | (opcional) onde salvar o progresso; padrão `watcher-offsets.json` |

## Verificação de integridade

```
SHA-256: 016f4aed626274af21b2914b50a1e37be9e74e2a4ce6e42ea02165a12b84b37a
```

Confira no PowerShell:
```powershell
Get-FileHash dommo-sync.exe -Algorithm SHA256
```
