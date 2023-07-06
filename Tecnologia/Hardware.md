sobre manutenção e montagem de computadores:
sobre programas para manutenção/reparação/diagnósticos de máquinas:
programas básicos - chrome, winrar, libre office.
cpu-l -> aplicativo para ver processadores
cpu-z -> aplicativo para ver definições dos hardwares da máquina
quais as mudanças de x32/x84 para 64b?
32 trabalha apenas com 4gb de ram
diferença gpt e mbr?
pesquisar componente por id+data sheet geralmente no alldatasheet.com


Peças:

Montagem:
PLED -> Powerled
resetsw e pwrsw -> não importa polaridade
bunda do fan é a com astes
Placa-mãe bateria de 3voltz CR2032
pelo CARCMOS se inverter jumper ele zera bios para configuração de fábrica
ROM é o chip da bios
pci expressx16 -> 16 linhas de comunicação
tabela de pci 1 2 4 8 16 32
ponte sul virou chipset
ponte norte integrou no processador
tabela sata 1 2 3
super I/O monitora fan, temperatura, cuida dos barramentos também
o cristal de quartzo serve para gerar o clock do processador
temperatura máxima de 80ºC e voltagem máximade 1.4V

<details>
  <summary>

  ## Componentes :computer:
  </summary>

  ### Placa-Mãe

  ### Processador

  ### Cooler

  ### Memória RAM
  Random Access Memory
  É volátil, precisa de energia para manter dados.

  ### Fonte
  tabela de selo de eficiência
  como verificar se uma fonte está com curto circuito

  ### Placa de Vídeo
  Como verificar curto circuito

  ### HD SSD

</details>

Softwares e comunicação:
## BIOS & UEFI
Basic Input Output System e Unified Extensible Firmware Interface (mas também pode ser referenciado como bios).

A BIOS é um sistema básico da placa-mãe que configura algumas funções, como boot, leitura, clock, rotação de fans, temperatura, etc

### BIOS:
Lê apenas partições em mbr com limitação de 2TebaBytes
Possuí alguns problemas de segurança conhecidos
Não possuí suporte ao uso de mouse, limitada ao teclado

### UEFI
Inferface gráfica melhorada
Pode possuir suporte para mouse
Trabalha com partições MBR e GPT graças ao recurso de CSM(Compatibility Support Module) geralmente ativando o modo legacy


## Particionamento

### MBR
Master Boot Record
É uma forma de particionamento de disco (HD ou SSD) antiga usual até windows 8.1 e processadores 32bit.
Limitações
- Pode possuir leitura de até no máximo 2TeraBytes em uma partição (a parte acima do valor fica inutilizável e desconhecida pelo sistema)
- Não possuí compatibilidade com sistemas operacionais mais novos
- Permite máximo de 4 partições primárias em um disco, podendo possuir várias partições lógicas. Partições lógicas não possuem suporte para sistemas operacionais.

### GPT
GUID Partition Table

- Até 128 partições primárias no sistema windows e no sistema linux esse número pode ser maior
- Não funciona em sistemas 32bit ou sistemas anteriores à windows 8.1
- Limite de partição de até 9,4ZetaBytes



recomendado usar usb da propria placa e não gabinete para sistema operacional
teclado abnt2
diferença bpt e mbt?
padrao ntfs é padrão do windows, mac reconhece mas não consegue escrever nele,
fat 32 compatível com windows, linux, entre outros (pendrives)
como achar chave do windows
usar rufus para gravar pendrive

Manutenção:

Programas de diagnóstico:
programa lazersoft para recuperar senha windows
site heidoc para iso windows 7 ou torrent

