# Windows-Server-Core

   .SYNOPSIS
    HYPERV - Instalação de host Hyperv com Windows Server Core

## DESCRIPTION

	- Configurar Rede
 	- Firewall


.NOTES
    Autor: Leandro Melo Rosemberg
    Data: 19-02-2025
    Versão: 2.0
    Requisitos: PowerShell, Navegador

## Configurar Rede
Get-NetAdapter

## Firewall
	# para ativar ou desativar firewall para as redes de domínio, pública ou privada
	# desativar
	Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled False

	# ativar
	Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled True
