Instalando Linux (Kali Linux) no Windows com WSL

Passo 1: Verificar as distribuições Linux disponíveis
1- Abra o PowerShell como administrador.
2- Execute o comando abaixo para listar as distribuições disponíveis para instalação:
`wsl --list --online`

Passo 2: Instalar o Kali Linux
1- Para instalar o Kali Linux, execute o seguinte comando:
`wsl --install -d kali-linux`
2- Aguarde a conclusão da instalação. Ao final, o Kali Linux será baixado e configurado.
3- Assim que a instalação terminar, o terminal abrirá automaticamente para que você crie um nome de usuário e senha para o sistema.

Passo 3: Instalar o ambiente de desktop XFCE e o servidor RDP
1- Instale o ambiente de desktop XFCE:
`sudo apt update`
`sudo apt install kali-desktop-xfce`
2- Instale o servidor RDP (Remote Desktop Protocol):
`sudo apt install xrdp`

Passo 4: Configurar o servidor XRDP
1- Configure o servidor para iniciar o XFCE automaticamente:
`echo "startxfce4" > ~/.xsession`
2- Inicie o serviço XRDP:
`sudo service xrdp start`
3- Configure o XRDP para iniciar automaticamente com o sistema:
`sudo systemctl enable xrdp`

Passo 5: Obter o endereço IP
1- Verifique o endereço IP da máquina para conectar-se ao RDP:
Utilize um dos comandos abaixo:
`ifconfig`
ou
`ip a`
2- Anote o endereço IP exibido no terminal.

Passo 6: Conectar ao ambiente de desktop via RDP
1- Abra o aplicativo Conexão de Área de Trabalho Remota no Windows.
2- Digite o endereço IP obtido anteriormente e clique em Conectar.
3- Insira seu nome de usuário e senha criados no Kali Linux para acessar o ambiente XFCE.

## Aviso:  1-  Você pode instalar outras distribuições Linux listadas no comando wsl --list --online, caso não queira usar o Kali Linux.
## 2-  caso queira ficar utilizando constantemente seu kali ou linux ele salva tudo que você utilizar ou fizer, ficar salvo na maquina a não ser que realize o processo de deletar ela.
## 3- pra caso quiser ficar utilizando ela varias vezes após a instalação basta seguir o passo 4 pra quando quiser subir a interface grafica
Segue o video abaixo de bem basico demostrando como utilizar os comandos
