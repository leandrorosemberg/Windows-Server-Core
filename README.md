# Windows-Server-Core

   .SYNOPSIS
    HYPERV - Instalação de host Hyperv com Windows Server Core

## DESCRIPTION

	- Configurar Rede
	- Configurar no dominio 
	- Configurações de disco
 	- Firewall


.NOTES
    Autor: Leandro Melo Rosemberg
    Data: 19-02-2025
    Versão: 2.0
    Requisitos: PowerShell, Navegador

## Configurar Rede
Get-NetAdapter

## Firewall
	# desativar firewall
	Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled False
