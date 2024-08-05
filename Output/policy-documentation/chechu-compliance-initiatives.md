# Document Initiatives

Auto-generated Policy effect documentation for PolicySets grouped by Effect and sorted by Policy category and Policy display name.

## Policy Set (Initiative) List

### AKV

- Display name: Guardrails-AKV-Security-CIS2.0

- Type: Custom
- Category: Key Vault

This initiative groups all key vault policies defined by the SCC (CIS 2.0) to ensure compliance and security of their key vault.

### CDB-jasl

- Display name: Guardarails-CDB-testjasl

- Type: Custom
- Category: Unknown

politicas excepciones mitgacion parcial de un recurso.


## Policy Effects

| Category | Policy | AKV | CDB-jasl |
| :------- | :----- | :-------: | :-------: |
| App Configuration | **JASL-Configure App Configuration to disable public network access**<br/>Disable public network access for App Configuration so that it isn't accessible over the public internet. This configuration helps protect them against data leakage risks. You can limit exposure of the your resources by creating private endpoints instead. Learn more at: https://aka.ms/appconfig/private-endpoint. |  | **Modify**<br/>Disabled |
| Cosmos DB | **CDB Disable localAuth jasl**<br/>Disable local authentication methods so that your Cosmos DB database accounts exclusively require Azure Active Directory identities for authentication. Learn more at: https://docs.microsoft.com/azure/cosmos-db/how-to-setup-rbac#disable-local-auth. |  | **Audit**<br/>Deny<br/>Disabled |
| Databases | **MSS Disable localAuth jasl.**<br/>Disable local authentication methods so that your MSS DBforMySQL. |  | **Deny**<br/>Disabled |
| Key Vault | **Azure Key Vault should use RBAC permission model**<br/>Enable RBAC permission model across Key Vaults. Learn more at: https://learn.microsoft.com/en-us/azure/key-vault/general/rbac-migration | **Audit**<br/>Deny<br/>Disabled |  |
| Key Vault | **Key Vault keys should have an expiration date**<br/>Cryptographic keys should have a defined expiration date and not be permanent. Keys that are valid forever provide a potential attacker with more time to compromise the key. It is a recommended security practice to set expiration dates on cryptographic keys. | **Audit**<br/>Deny<br/>Disabled |  |
| Key Vault | **Key Vault secrets should have an expiration date**<br/>Secrets should have a defined expiration date and not be permanent. Secrets that are valid forever provide a potential attacker with more time to compromise them. It is a recommended security practice to set expiration dates on secrets. | **Audit**<br/>Deny<br/>Disabled |  |
| Key Vault | **Key vaults should have deletion protection enabled**<br/>Malicious deletion of a key vault can lead to permanent data loss. You can prevent permanent data loss by enabling purge protection and soft delete. Purge protection protects you from insider attacks by enforcing a mandatory retention period for soft deleted key vaults. No one inside your organization or Microsoft will be able to purge your key vaults during the soft delete retention period. Keep in mind that key vaults created after September 1st 2019 have soft-delete enabled by default. | **Audit**<br/>Deny<br/>Disabled |  |
| Key Vault | **Key vaults should have soft delete enabled**<br/>Deleting a key vault without soft delete enabled permanently deletes all secrets, keys, and certificates stored in the key vault. Accidental deletion of a key vault can lead to permanent data loss. Soft delete allows you to recover an accidentally deleted key vault for a configurable retention period. | **Audit**<br/>Deny<br/>Disabled |  |

## Policy Parameters by Policy

| Category | Policy | AKV | CDB-jasl |
| :------- | :----- | :------- | :------- |
