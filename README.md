# Windows-Server-Core
    HYPERV - Instalação de host Hyperv com Windows Server Core
    Requisitos: PowerShell
    
## DESCRIPTION

	- Configurar Rede
 	- Firewall


## Configurar Rede
Get-NetAdapter

## Firewall
	
 	Ativar ou desativar firewall para as redes de domínio, pública ou privada
 
	# desativar
	Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled False

	# ativar
	Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled True
