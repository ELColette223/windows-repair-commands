# Windows Repair Commands
PT-BR: Este Repositório contem comandos de recuperação para Windows 7, 8, 8.1, 10 e 11. Está dividido em Inglês e Português Brasil.

EN: This Repository contains recovery commands for Windows 7, 8, 8.1, 10 and 11. It is divided into English and Brazilian Portuguese.

# English

This repository contains recovery commands for Windows 7, 8, 8.1, 10, and 11. With these commands, you can easily repair your Windows installation without the need to restore it.

## Open Command Prompt in Windows 7
1. Restart your computer.
2. While the computer is restarting, press the F8 key repeatedly before the Windows logo appears.
3. Choose "Safe Mode with Command Prompt".

## Open Command Prompt in Windows 8, 8.1, 10, and 11
1. Restart your computer: First, you need to restart your computer.
2. Access Advanced Startup Options: There are several ways to access the advanced startup options:
   - Method 1: **In Windows 8 and 8.1**, you can hold the Shift key while clicking "Restart" in the Start menu or on the login screen. In **Windows 10 and 11**, you can click the "Restart" button while holding the Shift key in the Start menu.
   - Method 2: **In Windows 8, 8.1, 10, and 11**, you can also open "Run" (Press "Win + R") and type `shutdown.exe /r /o /f /t 00`, then press Enter. **This will restart the computer into the advanced options**.

3. Access Advanced Options: After the restart, you will be taken to the Advanced Startup Options.

4. Choose "Safe Mode with Command Prompt": Use the arrow keys to navigate and select the "Safe Mode with Command Prompt" option or something similar in the advanced options.

5. Once Command Prompt is open, proceed to the next steps.

## Windows 7, 8, 8.1, 10, and 11

Below are some commands for recovering Windows 7, 8, 8.1, 10, and 11 along with their explanations.

### Command to check disk errors:
```bash
chkdsk /f /r d:
```
Replace `d:` with the appropriate local disk directory.

### Command to scan and fix corrupted files:
```bash
sfc /scannow
```
If any issues are detected, execute the following command:
```bash
/offbootdir-c:\ /offwindir=d:\windows
```

### Command to remove corrupted updates:
```bash
dism.exe /image:d:\ /cleanup-image /revertpendingactions
```

### Command to check system integrity and fix errors:
```bash
dism.exe /online /cleanup-image /restorehealth
```

### Command to fix boot and MBR issues:
```bash
bootrec.exe /fixmbr
```

```bash
bootrec.exe /fixboot
```

### Command to recreate the BCD (Boot Configuration Data):
```bash
bootrec.exe /rebuildbcd
```

## Tips

### Keep your antivirus updated and always active:
1. Select **Start  > Settings  > Update & Security  > Windows Security > Virus & threat protection**.
2. Select **Check for updates** (or **Check for updates for threat protection** in older versions of Windows 10).
3. Under **Threat settings**, select **Check for updates**.
4. If Windows Security finds a new signature, it will download and install it.
5. The update is complete with the new signature. Keep these points in mind.

### For Windows 7, 8, and 8.1, use an antivirus:
I recommend using one of the following antiviruses:
- Avast Free Antivirus.
- Bitdefender Antivirus Free Edition.
- Kaspersky Security Cloud Free.

**CAUTION: Never use cracked or modified antivirus software!**

### Create a recovery drive for your Windows:
1. Search for **Create a recovery drive**.
2. Make sure to back up system files to the recovery drive and select Next.
3. Connect a USB drive to your computer, select it, and select Next.
4. Select Create. Many files need to be copied to the recovery drive, so this might take a while.

### Create a restore point for your Windows:
1. In the search box on the taskbar, type **Create a restore point**. In Windows 7: **Click on Start -> Control Panel -> System and Security -> System -> System Protection -> Create...**
2. Name the restore point.
3. Click Create.

# Programs I do not recommend installing (Personal opinion)

First of all, this is just a personal recommendation. Some of these programs can cause slowness or issues in your Windows, speaking from personal experience.

- **Driver Booster** or any driver update program.
   - In addition to Windows itself automatically finding all the drivers, this program has proven to be a major problem, causing computer slowness with its background processes!

- **CCleaner**
   - First and foremost, CCleaner is not completely useless. It can save a lot of work by removing files, but that's about it. For other things like "cleaning the registry," "optimizing the system," and everything it promises, it's of no use!

# Português Brasil

## Abrir prompt de comando Windows 7.
1. Reinicie o Computador
2. Enquanto o Computador reinicia pressione repetidamente a tecla F8 do teclado antes de aparecer a logo do Windows.
3. Escolha "Modo de Segurança com Prompt de Comando".

## Abrir prompt de comando Windows 8, 8.1, 10 e 11.
1. Reinicie o Computador: Primeiro, você precisará reiniciar o seu computador.

2. Acesse as Opções de Inicialização Avançada: Existem algumas maneiras de acessar as opções de inicialização avançada:
   1. Método 1: **No Windows 8 e 8.1**, você pode segurar a tecla Shift enquanto clica em "Reiniciar" no Menu Iniciar ou na tela de login. No **Windows 10 e 11**, você pode clicar no botão "Reiniciar" enquanto mantém a tecla Shift pressionada no menu Iniciar.

   2. Método 3: **No Windows 8, 8.1, 10 e 11**, você também pode abrir o "Executar" (Pressione "Win + R") e digitar ```shutdown.exe /r /o /f /t 00```, e depois pressione Enter. **Isso reiniciará o computador nas opções avançadas.**

3. Acesse as Opções Avançadas: Após o reinício, você será levado às Opções Avançadas de Inicialização.

4. Escolha "Modo de Segurança com Prompt de Comando": Use as setas do teclado para navegar e selecione a opção "Modo de Segurança com Prompt de Comando" ou algo similar nas opções avançadas.

5. Com o Prompt de Comando já aberto prossiga para as próximas etapas.
## Windows 7, 8, 8.1, 10 e 11

Abaixo estão alguns comandos para recuperação do Windows 7, 8, 8.1, 10 e 11 juntamente com as explicações.

### Comando para verificar erros no disco:
```bash
chkdsk /f /r d:
```
Substitua `d:` pelo diretório do disco local correspondente.

### Comando para verificar e corrigir arquivos corrompidos:
```bash
sfc /scannow
```
Se houver algum problema, execute o seguinte comando:
```bash
/offbootdir-c:\ /offwindir=d:\windows
```

### Comando para remover atualizações corrompidas:
```bash
dism.exe /image:d:\ /cleanup-image /revertpendingactions
```
### Comando para verificar a integridade do sistema e corrigir erros:

```bash
dism.exe /online /cleanup-image /restorehealth
```

### Comando para corrigir problemas de inicialização e MBR:
```bash
bootrec.exe /fixmbr
```

```bash
bootrec.exe /fixboot
```

### Comando para recriar o BCD (Boot Configuration Data):

```bash
bootrec.exe /rebuildbcd
```

## Dicas
### Deixe seu antivírus atualizado e sempre ativo:

1. Selecione **Iniciar  > Configurações  > Atualização e Segurança  > Segurança do Windows > Proteção contra vírus e ameaças**.
2. Selecione **Verificar se há atualizações** (ou **Atualizações da proteção contra vírus e ameaças** em versões anteriores do Windows 10).
3. Em **Definições de ameaça**, selecione **Verificar se há atualizações**.
4. Se a Segurança do Windows encontrar uma nova assinatura, ela irá baixá-la e instalá-la.
5. A atualização estará concluída com a nova assinatura. Tenha esses pontos em mente. 

### Windows 7, 8 e 8.1, use um antivírus:
Recomendo o uso de um dos seguintes antivírus:
- Avast Free Antivirus.
- Bitdefender Antivirus Free Edition.
- Kaspersky Security Cloud Free.

**ATENÇÃO: Nunca use antivírus crackeado ou modificado!**

### Crie uma unidade de recuperação de seu Windows:

1. Pesquise por **Criar uma unidade de recuperação**
2. Certifique-se de fazer backup dos arquivos do sistema para a unidade de recuperação e selecione Avançar.
3. Conecte uma unidade USB ao computador, selecione-a e selecione Avançar.
4. Selecione Criar. Muitos arquivos precisam ser copiados para a unidade de recuperação, portanto, isso pode demorar um pouco.

### Crie um ponto de restauração de seu Windows
1. Na caixa de pesquisa na barra de tarefas, digite **Criar um ponto de restauração**. No caso do Windows 7: **Clique no iniciar -> Painel de Controle -> Sistema e Segurança -> Sistema -> Proteção do Sistema -> Criar...**
2. Nomeie o ponto de restauração.
3. Clique em Criar.

# Programas que não recomendo instalar (Opinião pessoal).
Antes de mais nada, isso é apenas uma recomendação pessoal, alguns destes programas podem causar lentidão ou problemas no seu Windows, falo isso por experiência própria.

- **Driver Booster** ou qualquer programa de atualização de drivers. 
  - Além do próprio Windows encontrar todos os drivers automaticamente, este programa já se mostrou ser um grande problema causando lentidão no computador com seus processos que rodam de fundo!

- **CCleaner**
  - Antes de mais nada, o CCleaner não é totalmente inútil, ele consegue poupar um grande trabalho em remover arquivos, mas apenas isso, para outras coisas como "limpar registro", "Otimizar sistema" e tudo que ele promete, não serve para nada!
