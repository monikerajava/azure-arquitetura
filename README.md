# azure-arquitetura
Este projeto você entenderá como se concentra os componentes essenciais da arquitetura do Azure.

# 🌍 Arquitetura do Azure e Organização de Recursos

Este resumo aborda os principais conceitos do módulo 2 da preparação para a certificação **AZ-900**, com foco em **regiões do Azure**, **data centers**, **grupos de recursos**, **controle de acesso**, e **criação de redes virtuais (VNet)**.

---

## 🗺️ Infraestrutura Global do Azure

- O Azure possui mais de **60 regiões distribuídas globalmente**.
- Regiões são conjuntos de data centers que permitem:
  - **Alta disponibilidade**
  - **Baixa latência**
  - **Resiliência geográfica**

### 🌎 Visualização da Infraestrutura

- Acesse o portal: [https://infrastructure.microsoft.com](https://infrastructure.microsoft.com)
- Use o botão **"Explore the Globe"** para:
  - Visualizar data centers ativos e planejados.
  - Realizar um **tour virtual em um data center Microsoft**.
  - Entender como os data centers funcionam em termos de segurança, sustentabilidade e operação.

### 🇧🇷 Regiões no Brasil

- **Brazil South (São Paulo)** – Disponível para todos os clientes.
- **Brazil Southeast (Rio de Janeiro)** – Usada para cenários de **Disaster Recovery** e **compliance com LGPD**.
- Algumas replicações ainda ocorrem para fora do país (ex: EUA), exceto quando contratualmente configurado para **residência de dados nacional**.

---

## 🧱 Grupos de Recursos (Resource Groups)

- **Definição**: Coleção lógica de recursos que compartilham o mesmo ciclo de vida.
- **Exemplo de uso**: Nome `AZ900_LAB_RG` para centralizar recursos do laboratório.
- Permite organização por:
  - Projeto
  - Centro de custo
  - Ambiente (produção, dev, teste)

### 🏷️ Tagging (Marcação)

- Embora **opcional**, é **altamente recomendável**.
- Utilidade:
  - Identificação rápida de finalidade.
  - Facilita o rateio de custos na fatura.
  - Melhora a governança e o controle financeiro.

---

## 🔐 Controle de Acesso e Segurança

- Atribua **permissões mínimas necessárias** (princípio de menor privilégio).
- Use a aba **"Controle de Acesso (IAM)"** para:
  - Conceder/revogar permissões por grupo ou usuário.
  - Garantir que apenas pessoas autorizadas interajam com os recursos.

### 🚫 Bloqueios (Locks)

- Impedem a exclusão acidental de recursos críticos.
- Importante em ambientes colaborativos e com múltiplos administradores.

---

## 🌐 Criação de Rede Virtual (VNet)

- A VNet define o **endereço IP e a conectividade** de recursos no Azure.
- Etapas:
  1. Criar o grupo de recursos.
  2. Criar a **rede virtual** especificando:
     - Nome
     - Região
     - Endereçamento
  3. Vincular a recursos, como VMs.

### 🔁 Visualização e Gerenciamento

- O **visualizador de recursos** mostra uma árvore gráfica da arquitetura.
- A aba **Implantações** registra:
  - Templates usados (JSON)
  - Status e histórico
  - Tempo de execução e logs

---

## 🛠️ Templates de Automação

- Após criar um recurso pelo portal, é possível:
  - **Baixar o template JSON**
  - Reutilizar para automações futuras
- Exemplo:
  - Criou uma VNet? Faça o download do código e customize para novos ambientes.

---

## ✅ Boas Práticas

- Explore o **portal manualmente antes de automatizar**.
- Estude a documentação oficial do Azure para entender limitações e boas práticas.
- Nunca assuma que os recursos ou permissões permanecem estáticos — o ambiente de nuvem é **altamente dinâmico**.

---

> _"A nuvem é poderosa, mas exige organização, governança e boas práticas para ser usada com eficiência."_ ☁️

