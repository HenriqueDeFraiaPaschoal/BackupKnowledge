Limpeza de disco mensal
botão direito no iniciar -> windows powershell

CHKDSK /r || /s -> verificar disco

sfc /scannow -> corrige arquivos protegidos do windows

dism /online /cleanup-image /restorehealth -> rerificar arquivos windows

desfragmentar disco em caso de HD

windows update

painel de controle -> aplicativos e desinstalar não usado e desabilitar inicializações de aplicativos não necessárias

personalizar para alto desempenho em caso de notebook

windows pendrive minimo 8gb
recomendado usar usb da propria placa e não do gabinete

padrao ntfs é padrão do windows

# Windows

## Instalação

## Comandos
Os comandos podem podem ser executando abrindo o prompt de comando ou PowerShell como admin.
Não é recomendado para os comandos durante sua execução. Alguns comandos podem levar horas em caso de HD.
Onde "C" será a partição desejada a executar o comando.

- CHKDSK /r -> Verifica e corrige falhas no disco reiniciando ou na próxima reinicialização do sistema
- SFC /SCANNOW -> Verifica e corrige arquivos protegidos do windows
- DISM /ONLINE /CLEANUP-IMAGE /RESTOREHEALTH -> Verifica e corrige arquivos corrompidos do windows
- c:\windows\SYSTEM32\cleanmgr.exe /d"Unidade" -> Executa limpeza de disco
- Desfragmentar disco -> Deixa os arquivos organizados de maneira que o acesso seja mais rápido
- compact.exe /CompactOS:query -> compact.exe /CompactOS:Always -> recupera espaço no HD?
