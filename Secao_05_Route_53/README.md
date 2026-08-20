# Seção 05 — Route 53

Documentação da seção de Route 53 do curso **AWS na Prática**.

## Português (Brasil)

Esta seção aborda os fundamentos de DNS (Domain Name System) e gerenciamento de domínios na AWS com Amazon Route 53, incluindo criação de zonas hospedadas, registros de DNS, políticas de roteamento, health checks e transferência de tráfego inteligente.

### Texto corrido para estudo

Nesta seção, o estudo começa com a introdução ao Amazon Route 53, um serviço de DNS gerenciado e registrador de domínios da AWS. O conteúdo apresenta o console do Route 53 e como navegá-lo para gerenciar domínios e registros DNS.

Na sequência, a seção aborda a criação de zonas hospedadas privadas, que permitem resolver nomes de domínio dentro de uma VPC sem expor os serviços à internet. Depois, o material mostra como criar zonas hospedadas públicas, tornando um domínio acessível na internet, incluindo a importação de registros de DNS e a criação manual de registros.

O conteúdo aprofunda com a compreensão entre registros de alias e não-alias, destacando os benefícios de usar registros de alias do Route 53 para integração com recursos AWS. Em seguida, apresenta health checks, que monitoram a saúde de recursos e endpoints, permitindo roteamento inteligente baseado em disponibilidade.

A seção então explora as políticas de roteamento disponíveis no Route 53: roteamento simples (simple), ponderado (weighted), failover, geolocalização, latência, multivalor e baseado em IP (IP-based), além de geoproximidade. Cada política é apresentada com seus casos de uso e configuração prática.

Por fim, o material aborda o Traffic Flow, uma ferramenta visual para criar e gerenciar políticas de roteamento complexas, e o processo de registro de novo domínio diretamente no Route 53, fornecendo uma trilha completa para gerenciar DNS, domínios e tráfego na AWS.

### Resumo dos arquivos

- `Slides/10_1_IntroducaoRoute53.pdf`: introdução ao Amazon Route 53.
- `Slides/10_2_R53Console.pdf`: navegação e uso do console Route 53.
- `Slides/10_3_CriandoDominioPrivado.pdf`: criação de zonas hospedadas privadas.
- `Slides/10_4_ImportandoRegistros.pdf`: importação de registros DNS.
- `Slides/10_5_CriandoDominioPublico.pdf`: criação de domínios públicos no Route 53.
- `Slides/10_6_Alias.pdf`: compreensão e uso de registros de alias.
- `Slides/10_7_HealthChecks.pdf`: configuração e monitoramento de health checks.
- `Slides/10_8_PoliticasDeRoteamento.pdf`: visão geral das políticas de roteamento.
- `Slides/10_9_FailoverPolicy.pdf`: política de roteamento por failover.
- `Slides/10_10_PonderadoPolicy.pdf`: política de roteamento ponderada (weighted).
- `Slides/10_11_GeolocationPolicy.pdf`: política de roteamento por geolocalização.
- `Slides/10_12_LatencyPolicy.pdf`: política de roteamento por latência.
- `Slides/10_13_MultivaluePolicy.pdf`: política de roteamento multivalor.
- `Slides/10_14_IPPolicy.pdf`: política de roteamento baseada em IP.
- `Slides/10_15_GeoproximidadePolicy.pdf`: política de roteamento por geoproximidade.
- `Slides/10_16_FluxoTrafego.pdf`: Traffic Flow no Route 53.
- `Slides/10_17_RegisterDomain.pdf`: registro de novos domínios.
- `Links/Links.txt`: links e referências oficiais da seção.

### Arquivos

| Arquivo | Descrição |
|---|---|
| `Slides/10_1_IntroducaoRoute53.pdf` | Introdução ao Amazon Route 53. |
| `Slides/10_2_R53Console.pdf` | Console do Route 53. |
| `Slides/10_3_CriandoDominioPrivado.pdf` | Criação de zonas hospedadas privadas. |
| `Slides/10_4_ImportandoRegistros.pdf` | Importação de registros DNS. |
| `Slides/10_5_CriandoDominioPublico.pdf` | Criação de domínios públicos. |
| `Slides/10_6_Alias.pdf` | Registros de alias no Route 53. |
| `Slides/10_7_HealthChecks.pdf` | Health checks e monitoramento. |
| `Slides/10_8_PoliticasDeRoteamento.pdf` | Políticas de roteamento disponíveis. |
| `Slides/10_9_FailoverPolicy.pdf` | Roteamento com failover. |
| `Slides/10_10_PonderadoPolicy.pdf` | Roteamento ponderado (weighted). |
| `Slides/10_11_GeolocationPolicy.pdf` | Roteamento por geolocalização. |
| `Slides/10_12_LatencyPolicy.pdf` | Roteamento por latência. |
| `Slides/10_13_MultivaluePolicy.pdf` | Roteamento multivalor. |
| `Slides/10_14_IPPolicy.pdf` | Roteamento baseado em IP. |
| `Slides/10_15_GeoproximidadePolicy.pdf` | Roteamento por geoproximidade. |
| `Slides/10_16_FluxoTrafego.pdf` | Traffic Flow e políticas visuais. |
| `Slides/10_17_RegisterDomain.pdf` | Registro de novos domínios. |
| `Links/Links.txt` | Referências oficiais e materiais de apoio. |

## English

This section covers DNS (Domain Name System) fundamentals and domain management on AWS with Amazon Route 53, including hosted zone creation, DNS records, routing policies, health checks, and intelligent traffic management.

### Continuous study text

This section begins with an introduction to Amazon Route 53, AWS's managed DNS service and domain registrar. The content walks through the Route 53 console and how to navigate it for managing domains and DNS records.

Next, the section covers private hosted zones, which allow resolving domain names within a VPC without exposing services to the internet. The material then demonstrates creating public hosted zones to make a domain accessible on the internet, including importing DNS records and manually creating records.

The content deepens with understanding the differences between alias and non-alias records, highlighting the benefits of using Route 53 alias records for AWS resource integration. It then introduces health checks, which monitor resource and endpoint health, enabling intelligent routing based on availability.

The section then explores the available routing policies in Route 53: simple routing, weighted, failover, geolocation, latency, multivalue, and IP-based routing, as well as geoproximity. Each policy is presented with its use cases and practical configuration.

Finally, the material covers Traffic Flow, a visual tool for creating and managing complex routing policies, and the process of registering a new domain directly in Route 53, providing a complete foundation for managing DNS, domains, and traffic in AWS.

### File summary

- `Slides/10_1_IntroducaoRoute53.pdf`: introduction to Amazon Route 53.
- `Slides/10_2_R53Console.pdf`: Route 53 console overview and navigation.
- `Slides/10_3_CriandoDominioPrivado.pdf`: creating private hosted zones.
- `Slides/10_4_ImportandoRegistros.pdf`: importing DNS records.
- `Slides/10_5_CriandoDominioPublico.pdf`: creating public domains in Route 53.
- `Slides/10_6_Alias.pdf`: understanding and using alias records.
- `Slides/10_7_HealthChecks.pdf`: configuring and monitoring health checks.
- `Slides/10_8_PoliticasDeRoteamento.pdf`: overview of routing policies.
- `Slides/10_9_FailoverPolicy.pdf`: failover routing policy.
- `Slides/10_10_PonderadoPolicy.pdf`: weighted routing policy.
- `Slides/10_11_GeolocationPolicy.pdf`: geolocation-based routing policy.
- `Slides/10_12_LatencyPolicy.pdf`: latency-based routing policy.
- `Slides/10_13_MultivaluePolicy.pdf`: multivalue answer routing policy.
- `Slides/10_14_IPPolicy.pdf`: IP-based routing policy.
- `Slides/10_15_GeoproximidadePolicy.pdf`: geoproximity routing policy.
- `Slides/10_16_FluxoTrafego.pdf`: Traffic Flow in Route 53.
- `Slides/10_17_RegisterDomain.pdf`: registering new domains.
- `Links/Links.txt`: official links and references.

### Files

| File | Description |
|---|---|
| `Slides/10_1_IntroducaoRoute53.pdf` | Introduction to Amazon Route 53. |
| `Slides/10_2_R53Console.pdf` | Route 53 console overview. |
| `Slides/10_3_CriandoDominioPrivado.pdf` | Creating private hosted zones. |
| `Slides/10_4_ImportandoRegistros.pdf` | Importing DNS records. |
| `Slides/10_5_CriandoDominioPublico.pdf` | Creating public domains. |
| `Slides/10_6_Alias.pdf` | Alias records in Route 53. |
| `Slides/10_7_HealthChecks.pdf` | Health checks and monitoring. |
| `Slides/10_8_PoliticasDeRoteamento.pdf` | Available routing policies. |
| `Slides/10_9_FailoverPolicy.pdf` | Failover routing. |
| `Slides/10_10_PonderadoPolicy.pdf` | Weighted routing policy. |
| `Slides/10_11_GeolocationPolicy.pdf` | Geolocation-based routing. |
| `Slides/10_12_LatencyPolicy.pdf` | Latency-based routing. |
| `Slides/10_13_MultivaluePolicy.pdf` | Multivalue answer routing. |
| `Slides/10_14_IPPolicy.pdf` | IP-based routing. |
| `Slides/10_15_GeoproximidadePolicy.pdf` | Geoproximity-based routing. |
| `Slides/10_16_FluxoTrafego.pdf` | Traffic Flow and visual policies. |
| `Slides/10_17_RegisterDomain.pdf` | Registering new domains. |
| `Links/Links.txt` | Official references and support material. |
