## 🛡️ Gestão de Usuários e Segurança no Google Workspace

Este repositório reúne as diretrizes e boas práticas implementadas para a governança de identidades e proteção de dados no ambiente do Google Workspace. O foco inicial da estrutura de segurança está baseado em três pilares fundamentais:

### 1. Autenticação Forte (MFA / 2SV)
* **Objetivo:** Mitigar riscos de sequestro de contas e ataques de *phishing*.
* **Ação:** Imposição de **Verificação em Duas Etapas (2SV)** para todos os usuários da organização, priorizando o uso de chaves físicas de segurança (FIDO2), prompts do Google e aplicativos de autenticação (MFA).

### 2. Autenticação e Proteção de E-mail (DNS)
Implementação de protocolos de segurança na zona de DNS para garantir a entregabilidade dos e-mails e evitar ataques de *spoofing* (falsificação de identidade):
* **SPF:** Definição dos servidores autorizados a enviar e-mails em nome do domínio corporativo.
* **DKIM:** Assinatura criptográfica que atesta a integridade e a origem das mensagens enviadas.
* **DMARC:** Política de conformidade para instruir servidores de destino sobre como agir (monitorar, quarentena ou rejeitar) caso e-mails falhem no SPF/DKIM.

### 3. Governança de Dados (Google Drive)
* **Objetivo:** Prevenção contra o vazamento de informações confidenciais (DLP).
* **Ação:** Configuração de políticas de compartilhamento externo granulares por Unidades Organizacionais (OUs), restringindo o acesso público a links e limitando o compartilhamento de arquivos sensíveis apenas a domínios confiáveis (Lista Branca).
