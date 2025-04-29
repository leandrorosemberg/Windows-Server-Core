# Windows-Server-Core
    HYPERV - Instalação de host Hyperv com Windows Server Core
    Requisitos: PowerShell
    
## DESCRIPTION

	- Configurar Rede
 	- Firewall


## Configurar Rede
	#Listar os adaptadores de rede
	Get-NetAdapter

 	# Renomear Nome da Interface
  	Rename-NetAdapter -Name "NomeDaInterface" -NewName "NOVO_NOME_DA_NIC"

 	# Configurar IP
	New-NetIPaddress -InterfaceIndex "ID_DA_INTERFACE" -IPAddress "IP_DO_HOST" -PrefixLength "MASK" -DefaultGateway "GATEWAY"

 	# Configurar DNS
  	Set-DNSClientServerAddress –InterfaceIndex "X" -ServerAddresses "IP_DNS_PRIMARIO,IP_DNS_SECUNDARIO"

   	# Configurar VLAN	
    	Set-NetAdapter -Name "NomeDaInterface" -vlanid "ID_DA_VLAN"
     
     	# Desativar IPV6 (todas as interfaces)
	Disable-NetAdapterBinding -Name "*" -ComponentID ms_tcpip6





## Firewall
	
 	# Ativar ou desativar firewall para as redes de domínio, pública ou privada
	# desativar
	Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled False
	# ativar
	Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled True
