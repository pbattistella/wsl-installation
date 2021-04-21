# Instalação do WSL no Windows 10

# Pré-condições
Veja se seu Windows 10 está na versão 2004 ou superior.
## Para verificar a versão acesse:

-Menu de Notificações (próximo ao relógio do windows)

-Todas as configurações

-Sistema

-Sobre

Caso não seja a versão 2004, baixe ela: https://go.microsoft.com/fwlink/?LinkID=799445

## Habilete o WSL para rodar no Windows 10

### Abra o Windows Terminal ou PowerShell como ADMINISTRADOR e execute os seguintes comandos:

dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

(Referência dos passos acima caso tenha dúvida: https://github.com/codeedu/wsl2-docker-quickstart)

# Baixando e instalando o Ubuntu manualmente

Digite no Windows Terminal ou PowerShell.
### Criar pasta do ubuntu no disco desejado:

mkdir d:\ubuntu

### Entrar na pasta do ubuntu:

cd d:\ubuntu

O comando abaixo vai fazer o download do ubuntu 20.04 no formato appx(app do windows)
Verifique a última versão no site: https://docs.microsoft.com/pt-br/windows/wsl/install-manual

### Digite no no Windows Terminal:

Invoke-WebRequest -Uri https://aka.ms/wslubuntu2004 -OutFile Ubuntu.appx -UseBasicParsing

### Renomeie o arquivo abaixo para formato zip:

Rename-Item .\Ubuntu.appx Ubuntu.zip

### Para extrair o arquivo zip use o comando:

Expand-Archive .\Ubuntu.zip -Verbose

### Entre no explorer (navegador de pastas do windows) e acesse o arquivo ubuntu2004.exe. 

Abrar o arquivo e experie ele instalar. No final você deverá inserir um username e password.

Depois você podera utilizar o Windows Terminal como terminal do linux sem problemas.
