# SOC Simulator - Phishing Investigation

## Overview

Investigação de um alerta de phishing utilizando Splunk em um ambiente simulado da TryHackMe.

## Alert Details

**Sender:**  
john@hatmakereurope.xyz

**Recipient:**  
michael.ascot@tryhatme.com

**Attachment:**  
ImportantInvoice-Febrary.zip

## Investigation

**Tool:**  
Splunk

**Queries:**

```spl
index=* "john@hatmakereurope.xyz"
```

Objetivo: Verificar eventos relacionados ao remetente.

```spl
index=* "ImportantInvoice-Febrary.zip"
```

Objetivo: Identificar ocorrências do arquivo anexado nos logs.

## Recommended Actions

- Remover o e-mail da caixa de entrada do usuário.
- Verificar se o usuário abriu o arquivo anexado.
- Analisar o arquivo anexado em um ambiente seguro.
- Bloquear o remetente caso seja confirmado como malicioso.

## Findings

- Remetente externo suspeito.
- Arquivo .zip em anexo.
- Indicadores de engenharia social.
- Possível tentativa de phishing.

## Classification

True Positive

## Escalation

Escalar o alerta e verificar possível comprometimento do usuário.
