# bsant-epac-jasl

Test EPAC model for Azure Policy

# Pasos a seguir
0. Creamos el repo vacio modo publico
1. crear infra MGs
2. instalar modulos PS
 2.1.   Install-Module Az -Scope CurrentUser
 2.2.   Install-Module EnterprisePolicyAsCode -Scope CurrentUser
 2.3. Poblamos el repo del paso 0 con carpetas. New-HydrationDefinitionFolder -DefinitionsRootFolder Definitions
3. Crear SP y asignarle rol Owner (en mi caso no puedo personalizar por no tener P1) al MG de EPAC-DEV. Tambien creamos el SP de PROD y haecmos la misma operacion.
4. Federamos siguiendo: https://learn.microsoft.com/en-us/entra/workload-id/workload-identity-federation-create-trust?pivots=identity-wif-apps-methods-azp#configure-a-federated-identity-credential-on-an-app
5. Modificamos el fichero C:\Github\Personal\000. MyGmailSuscription\EPAC-BSANT-PROD\bsant-enterprise-azure-policy-as-code\StarterKit\Definitions-GitHub-Flow\global-settings.jsonc siguiendo la configuracion de ejemplo <https://azure.github.io/enterprise-azure-policy-as-code/ci-cd-app-registrations/> y el blog de Rafa.
    5.1. New-Guid para meterlo en la linea 3    "pacOwnerId": 
6. He intentado utilizar este comando: New-PipelinesFromStarterKit -StarterKitFolder .\StarterKit -PipelinesFolder ..\bsant-epac-jasl\.github\workflows -PipelineType GitHubActions -BranchingFlow github -ScriptType Scripts Pero he tenido que poner Module al final porque no me descargaba la parte de scripts completa.
7. En cada Entorno de GITHUB. EPAC-DEV y EPAC-PROD creamos las variables de entorno. AZURE_CLIENT_ID (AppID) y AZURE_TENANT_ID 
