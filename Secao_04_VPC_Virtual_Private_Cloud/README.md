# Seção 04 — VPC (Virtual Private Cloud)

Documentação da seção de VPC do curso **AWS na Prática**.

## Português (Brasil)

Esta seção aborda os fundamentos de rede na AWS com Amazon VPC, incluindo criação de VPC e sub-redes, conectividade pública e privada, roteamento, gateways, emparelhamento, segurança de rede e integração híbrida.

### Texto corrido para estudo

Nesta seção, o estudo começa com a introdução ao Amazon VPC e com a análise da VPC padrão da conta, para entender como a AWS já entrega um ambiente inicial de rede. Em seguida, o conteúdo mostra a criação de uma VPC personalizada e de sub-redes, separando camadas públicas e privadas de acordo com as boas práticas de arquitetura. Depois, a seção aprofunda a conectividade, apresentando Internet Gateway e NAT Gateway para controlar saída e entrada de tráfego, além de testes práticos de comunicação entre sub-redes e recursos.

Na sequência, o material cobre associação de endereços IP elásticos, uso de prefix lists gerenciadas e DHCP option sets para padronizar configurações de rede e facilitar governança. Também entra no tema de VPC Endpoints com laboratório em EC2, mostrando como acessar serviços AWS de forma privada sem depender de internet pública. Em conectividade entre redes, a seção apresenta VPC Peering, com etapas de configuração e remoção, explicando rotas e regras necessárias para comunicação entre VPCs.

Por fim, são abordados controles de segurança em nível de sub-rede com NACL, proteção de consultas DNS com DNS Firewall e o cenário de integração híbrida com Site-to-Site VPN, fechando uma trilha completa para desenhar, proteger e operar redes na AWS com mais previsibilidade.

### Resumo dos arquivos

- `Slides/4_1_Introducao.pdf`: introdução ao Amazon VPC.
- `Slides/4_2_ConsoleDefaultVPC.pdf`: análise da VPC padrão no console.
- `Slides/4_3_CriandoVPC.pdf`: criação de VPC.
- `Slides/4_4_CriandoSubnets.pdf`: criação de sub-redes.
- `Slides/4_5_InternetGWxNATGW.pdf`: Internet Gateway versus NAT Gateway.
- `Slides/4_6_SubnetPublica.pdf`: conceitos de sub-rede pública.
- `Slides/4_7_SubnetsPrivadas.pdf`: conceitos de sub-redes privadas.
- `Slides/4_8_TestandoGateways.pdf`: testes de conectividade com gateways.
- `Slides/4_9_AssociacaoEnderecos.pdf`: associação de endereços IP.
- `Slides/4_10_PrefixLists.pdf`: prefix lists gerenciadas.
- `Slides/4_11_DHCPOptions.pdf`: DHCP option sets.
- `Slides/4_12_VPCEndpoints.pdf`: introdução a VPC Endpoints.
- `Slides/4_13_EC2VPCEndpoint.pdf`: laboratório EC2 com VPC Endpoint.
- `Slides/4_14_EC2VPCEndpoint.pdf`: aprofundamento/laboratório complementar de VPC Endpoint.
- `Slides/4_15_VPCPeeringSetup.pdf`: configuração de VPC Peering.
- `Slides/4_16_DeletandoVPCPeering.pdf`: remoção de VPC Peering.
- `Slides/4_17_NACL.pdf`: listas de controle de acesso de rede (NACL).
- `Slides/4_18_DNSFirewall.pdf`: DNS Firewall.
- `Slides/4_19_VPNSitetoSiteSimulacao.pdf`: simulação de VPN Site-to-Site.
- `Links/Links.txt`: links e referências oficiais da seção.

### Arquivos

| Arquivo | Descrição |
|---|---|
| `Slides/4_1_Introducao.pdf` | Introdução ao Amazon VPC. |
| `Slides/4_2_ConsoleDefaultVPC.pdf` | VPC padrão no console AWS. |
| `Slides/4_3_CriandoVPC.pdf` | Criação de VPC personalizada. |
| `Slides/4_4_CriandoSubnets.pdf` | Criação de sub-redes. |
| `Slides/4_5_InternetGWxNATGW.pdf` | Diferenças entre Internet Gateway e NAT Gateway. |
| `Slides/4_6_SubnetPublica.pdf` | Estrutura de sub-rede pública. |
| `Slides/4_7_SubnetsPrivadas.pdf` | Estrutura de sub-redes privadas. |
| `Slides/4_8_TestandoGateways.pdf` | Testes de conectividade com gateways. |
| `Slides/4_9_AssociacaoEnderecos.pdf` | Associação de endereços na VPC. |
| `Slides/4_10_PrefixLists.pdf` | Prefix lists gerenciadas. |
| `Slides/4_11_DHCPOptions.pdf` | Opções DHCP da VPC. |
| `Slides/4_12_VPCEndpoints.pdf` | Conceitos de VPC Endpoints. |
| `Slides/4_13_EC2VPCEndpoint.pdf` | Laboratório de VPC Endpoint com EC2. |
| `Slides/4_14_EC2VPCEndpoint.pdf` | Laboratório complementar de VPC Endpoint com EC2. |
| `Slides/4_15_VPCPeeringSetup.pdf` | Configuração de VPC Peering. |
| `Slides/4_16_DeletandoVPCPeering.pdf` | Remoção de VPC Peering. |
| `Slides/4_17_NACL.pdf` | NACL em sub-redes. |
| `Slides/4_18_DNSFirewall.pdf` | Proteção DNS com DNS Firewall. |
| `Slides/4_19_VPNSitetoSiteSimulacao.pdf` | Simulação de VPN Site-to-Site. |
| `Links/Links.txt` | Referências oficiais e materiais de apoio. |

## English

This section covers AWS networking fundamentals with Amazon VPC, including VPC and subnet creation, public/private connectivity, routing, gateways, peering, network security, and hybrid integration.

### Continuous study text

This section starts with an introduction to Amazon VPC and a review of the account default VPC, so you can understand the baseline network AWS provides out of the box. It then walks through creating a custom VPC and subnets, separating public and private layers according to common architecture practices. Next, it focuses on connectivity with Internet Gateway and NAT Gateway, including practical gateway tests to validate traffic flow between subnets and resources.

The material then covers Elastic IP association, managed prefix lists, and DHCP option sets to standardize network settings and improve governance. It also introduces VPC Endpoints with EC2-based labs, showing how to access AWS services privately without relying on public internet paths. For inter-network connectivity, the section presents VPC Peering setup and deletion, including the routing and rule adjustments required for VPC-to-VPC communication.

Finally, it covers subnet-level security controls with NACLs, outbound DNS filtering with DNS Firewall, and hybrid connectivity through Site-to-Site VPN simulation, closing with a practical foundation for designing, securing, and operating AWS networks.

### File summary

- `Slides/4_1_Introducao.pdf`: introduction to Amazon VPC.
- `Slides/4_2_ConsoleDefaultVPC.pdf`: default VPC overview in the console.
- `Slides/4_3_CriandoVPC.pdf`: creating a VPC.
- `Slides/4_4_CriandoSubnets.pdf`: creating subnets.
- `Slides/4_5_InternetGWxNATGW.pdf`: Internet Gateway vs NAT Gateway.
- `Slides/4_6_SubnetPublica.pdf`: public subnet concepts.
- `Slides/4_7_SubnetsPrivadas.pdf`: private subnet concepts.
- `Slides/4_8_TestandoGateways.pdf`: gateway connectivity tests.
- `Slides/4_9_AssociacaoEnderecos.pdf`: address association.
- `Slides/4_10_PrefixLists.pdf`: managed prefix lists.
- `Slides/4_11_DHCPOptions.pdf`: DHCP option sets.
- `Slides/4_12_VPCEndpoints.pdf`: VPC Endpoints introduction.
- `Slides/4_13_EC2VPCEndpoint.pdf`: EC2 VPC Endpoint lab.
- `Slides/4_14_EC2VPCEndpoint.pdf`: complementary EC2 VPC Endpoint lab.
- `Slides/4_15_VPCPeeringSetup.pdf`: VPC Peering setup.
- `Slides/4_16_DeletandoVPCPeering.pdf`: VPC Peering removal.
- `Slides/4_17_NACL.pdf`: Network ACLs.
- `Slides/4_18_DNSFirewall.pdf`: DNS Firewall.
- `Slides/4_19_VPNSitetoSiteSimulacao.pdf`: Site-to-Site VPN simulation.
- `Links/Links.txt`: official links and references.

### Files

| File | Description |
|---|---|
| `Slides/4_1_Introducao.pdf` | Introduction to Amazon VPC. |
| `Slides/4_2_ConsoleDefaultVPC.pdf` | Default VPC in AWS console. |
| `Slides/4_3_CriandoVPC.pdf` | Custom VPC creation. |
| `Slides/4_4_CriandoSubnets.pdf` | Subnet creation. |
| `Slides/4_5_InternetGWxNATGW.pdf` | Internet Gateway and NAT Gateway comparison. |
| `Slides/4_6_SubnetPublica.pdf` | Public subnet structure. |
| `Slides/4_7_SubnetsPrivadas.pdf` | Private subnet structure. |
| `Slides/4_8_TestandoGateways.pdf` | Gateway connectivity testing. |
| `Slides/4_9_AssociacaoEnderecos.pdf` | Address association in VPC. |
| `Slides/4_10_PrefixLists.pdf` | Managed prefix lists. |
| `Slides/4_11_DHCPOptions.pdf` | VPC DHCP options. |
| `Slides/4_12_VPCEndpoints.pdf` | VPC Endpoints concepts. |
| `Slides/4_13_EC2VPCEndpoint.pdf` | EC2 VPC Endpoint lab. |
| `Slides/4_14_EC2VPCEndpoint.pdf` | Complementary EC2 VPC Endpoint lab. |
| `Slides/4_15_VPCPeeringSetup.pdf` | VPC Peering setup. |
| `Slides/4_16_DeletandoVPCPeering.pdf` | VPC Peering deletion. |
| `Slides/4_17_NACL.pdf` | Subnet Network ACL controls. |
| `Slides/4_18_DNSFirewall.pdf` | DNS protection with DNS Firewall. |
| `Slides/4_19_VPNSitetoSiteSimulacao.pdf` | Site-to-Site VPN simulation. |
| `Links/Links.txt` | Official references and support material. |
