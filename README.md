# Batch to Bash
![Malware type](https://img.shields.io/badge/batch-windows-cyan)
![Malware type](https://img.shields.io/badge/bash-linux-black)

<div style="display: inline_block">
  <img align="center" alt="Linux" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/windows8/windows8-original.svg">
  <img align="center" alt="Linux" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg">
</div>

### Referências 
https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands

https://www.gnu.org/software/bash/manual/bash.html


| **Comando Batch (Windows)**            | **Comando Bash (Linux)**               |
|--------------------------------------|--------------------------------------------|
| `dir`                                | `ls`                                       |
| `cd nome_do_diretorio`               | `cd nome_do_diretorio`                     |
| `mkdir nome_do_diretorio`            | `mkdir nome_do_diretorio`                  |
| `del nome_do_arquivo`                | `rm nome_do_arquivo`                       |
| `rmdir nome_do_diretorio`            | `rmdir nome_do_diretorio` ou `rm -r nome_do_diretorio` |
| `copy arquivo_origem destino`        | `cp arquivo_origem destino`                |
| `move arquivo_origem destino`        | `mv arquivo_origem destino`                |
| `type nome_do_arquivo`               | `cat nome_do_arquivo`                      |
| `edit nome_do_arquivo`               | `nano nome_do_arquivo` (ou use `vim` ou `emacs`) |
| `ipconfig`                           | `ifconfig` ou `ip a`                      |
| `systeminfo`                         | `uname -a` ou `lsb_release -a` (para informações do sistema) |
| `tasklist`                           | `ps aux` ou `top`                         |
| `taskkill /IM nome_do_processo`      | `kill PID` (para encerrar um processo por ID) ou `pkill nome_do_processo` |
| `ping endereco_ip`                   | `ping endereco_ip`                        |
| `tracert endereco_ip`                | `traceroute endereco_ip` ou `tracepath endereco_ip` |
| `ipconfig /flushdns`                 | `sudo service nscd restart` (para reiniciar o serviço de cache DNS) |
| `netstat -a`                         | `ss -a` ou `netstat -a`                    |
| `chkdsk`                             | `fsck` (verificação e reparo de disco no Linux/Unix) |
| `sfc /scannow`                       | `sudo apt-get install --reinstall nome_do_pacote` |
| `gpupdate /force`                    | `sudo apt update && sudo apt upgrade -y`  |
| `shutdown /s /f /t 0`                | `shutdown now` ou `poweroff`              |
| `schtasks`                           | `crontab` (para agendar tarefas)          |
| `assoc`                              | `file` (para mostrar a associação de arquivo) |
| `ftype`                              | `file` (para mostrar o tipo de arquivo)    |
| `net use`                            | `mount` (para montar compartilhamentos de rede) |
| `net user`                           | `cat /etc/passwd` (para mostrar usuários)  |
| `net localgroup`                     | `getent group` (para mostrar grupos)       |
| `net view`                           | `showmount -e` (para mostrar compartilhamentos de rede) |
| `net share`                          | `exportfs -v` (para mostrar compartilhamentos exportados) |
| `netstat -an`                        | `ss -an` ou `netstat -an`                  |
| `format drive_letter:`               | `mkfs -t filesystem_type /dev/sdX` (para formatar uma partição) |
| `copy con nome_do_arquivo`           | `cat > nome_do_arquivo` (para criar um arquivo de texto) |
| `find /i "texto" arquivo.txt`        | `grep -i "texto" arquivo.txt`              |
| `xcopy /s diretorio_origem destino`  | `cp -r diretorio_origem destino`           |
| `robocopy origem destino /e`         | `rsync -a origem/ destino/`               |
| `attrib +h +s nome_do_arquivo`       | `chmod +h +s nome_do_arquivo`             |

## Criação, leitura, edição e remoção de itens 

Certamente, vou adicionar a indicação explícita do sistema operacional para cada comando:

- **Criar diretórios:**
  - Windows
    ```batch
    mkdir diretorio_1 diretorio_2
    ```
  - Linux
    ```bash
    mkdir diretorio_1 diretorio_2
    ```

- **Remover diretório:** 
  - Windows
    ```batch
    rmdir diretorio_1 diretorio_2
    ```
  - Linux
    ```bash
    rm -r diretorio_1 diretorio_2
    ```

- **Vizualizar diretórios e arquivos:** 
  - Windows
    ```batch
    dir item
    ```
  - Linux
    ```bash
    ls item
    ```

- **Filtrar vizualização de diretórios e arquivos:** 
  - Windows
    ```batch
    dir | findstr /i ".txt"
    ```
  - Linux
    ```bash
    ls | grep ".txt"
    ```

- **Mover diretórios e arquivos:** 
  - Windows
    ```batch
    move item destino
    ```
  - Linux
    ```bash
    mv item destino
    ```

- **Copiar diretórios e arquivos:** 
  - Windows
    ```batch
    copy item destino
    ```
  - Linux
    ```bash
    cp -r item destino
    ```

- **Deletar arquivo:** 
  - Windows
    ```batch
    del arquivo_1 arquivo_2
    ```
  - Linux
    ```bash
    rm arquivo_1 arquivo_2
    ```

- **Criar arquivos vazios:** 
  - Windows
    ```batch
    type nul > nota_vazia.txt
    ```
  - Linux
    ```bash
    touch nota_vazia.txt
    ```

- **Criar arquivos escritos:** 
  - Windows
    ```batch
    echo "oi" > nota.txt
    ```
  - Linux
    ```bash
    echo "oi" > nota.txt
    ```

- **Ler arquivos:** 
  - Windows
    ```batch
    type nota.txt
    ```
  - Linux
    ```bash
    cat nota.txt
    ```

