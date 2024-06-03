# bsant-epac-jasl

Test EPAC model for Azure Policy

# Pasos a seguir
0. Creamos el repo vacio modo publico
1. crear infra MGs
2. instalar modulos PS
 2.1.   Install-Module Az -Scope CurrentUser
 2.2.   Install-Module EnterprisePolicyAsCode -Scope CurrentUser
 2.3. Poblamos el repo del paso 0 con carpetas. New-HydrationDefinitionFolder -DefinitionsRootFolder Definitions
3. Crear SP y asignarle rol Owner (en mi caso no puedo personalizar por no tener P1) al MG de EPAC-DEV.
4. No he federado (probar sin este paso) <https://azure.github.io/enterprise-azure-policy-as-code/ci-cd-app-registrations/>
5. Modificamos el fichero C:\Github\Personal\000. MyGmailSuscription\EPAC-BSANT-PROD\bsant-enterprise-azure-policy-as-code\StarterKit\Definitions-GitHub-Flow\global-settings.jsonc siguiendo la configuracion de ejemplo <https://azure.github.io/enterprise-azure-policy-as-code/ci-cd-app-registrations/> y el blog de Rafa.
    5.1. New-Guid para meterlo en la linea 3    "pacOwnerId": 
     

