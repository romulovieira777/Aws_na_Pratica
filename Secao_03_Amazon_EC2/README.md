# Seção 03 — Amazon EC2

Documentação da seção de Amazon EC2 do curso **AWS na Prática**.

## Português (Brasil)

Esta seção cobre a base de uso do Amazon EC2, incluindo tipos de instância, modelos de aquisição, ciclo de vida, conexão por SSH, AMIs, Image Builder, tags, armazenamento EBS, snapshots, Elastic IP, Security Groups, Elastic Load Balancing, Auto Scaling, CloudShell, Session Manager, metadados da instância e `user-data`.

### Breve Resumo do conteúdo

Nesta seção, o estudo começa com a introdução ao Amazon EC2 e avança pelos principais conceitos necessários para usar instâncias de forma prática e segura. Primeiro, são apresentados os tipos de instância e os modelos de aquisição, para entender como escolher capacidade e custo conforme a necessidade. Em seguida, o conteúdo trata do ciclo de vida das instâncias, do uso de chaves SSH e da conexão com servidores Linux, criando a base para administração remota. Depois, a seção aprofunda o uso de AMIs, mostrando como criar, compartilhar e remover imagens, além de introduzir o EC2 Image Builder para automatizar a criação de imagens padronizadas. 

Na parte de organização e governança, o material explica o uso de tags para identificar recursos e facilitar o controle do ambiente. Em armazenamento, a seção aborda o EC2, os volumes EBS, os tipos de volume, a criação e anexação de discos e também os snapshots, incluindo permissões, ciclo de vida e a lixeira para recuperação. O conteúdo segue com Elastic IP e Security Groups, que ajudam a controlar endereçamento e acesso à rede. Depois, entra em Elastic Load Balancing, com foco em Application Load Balancer, target groups, roteamento, stickiness e HTTPS, além de um laboratório com `user-data` para automatizar a instalação do Nginx e disponibilizar uma aplicação de exemplo.

Por fim, a seção apresenta conceitos de Auto Scaling, launch templates, Auto Scaling Groups, políticas de escalonamento e integração com ALB, mostrando como manter aplicações disponíveis e adaptáveis à demanda. Também são vistos recursos como Instance Refresh, Console-to-Code, CloudShell, acesso via Session Manager, instâncias públicas, metadados da instância e problemas comuns relacionados a metadados, fechando com orientações e configurações globais para consolidar o uso do EC2 no dia a dia.

### Resumo dos arquivos

- `Slides/3_1_Introducao.pdf`: introdução ao Amazon EC2.
- `Slides/3_2_TiposDeInstanciasEC2.pdf`: tipos de instâncias do EC2.
- `Slides/3_3_ModelosDeAquisicao.pdf`: modelos de aquisição e compra de instâncias.
- `Slides/3_4_ModelosAquisicaoOverviewConsole.pdf`: visão geral dos modelos de aquisição no console.
- `Slides/3_6_CicloVidaInstanciasEC2.pdf`: ciclo de vida das instâncias EC2.
- `Slides/3_7_ChavesSSH.pdf`: criação e uso de chaves SSH.
- `Slides/3_8_ConectandoEmUmaInstanciaEC2.pdf`: conexão com instâncias EC2.
- `Slides/3_9_IntroducaoAMI.pdf`: introdução às AMIs.
- `Slides/3_11_CriandoAMI.pdf`: criação de AMIs.
- `Slides/3_12_CompartilhamentoDeAMI.pdf`: compartilhamento de AMIs.
- `Slides/3_13_RemovendoAMI.pdf`: remoção/cancelamento de AMIs.
- `Slides/3_14_IntroducaoEC2ImageBuilder.pdf`: introdução ao EC2 Image Builder.
- `Slides/3_15_CriandoBuilderPipeline.pdf`: criação de pipeline no Image Builder.
- `Slides/3_16_AWSTags.pdf`: uso de tags na AWS.
- `Slides/3_18_ArmazenamentoEC2.pdf`: armazenamento relacionado ao EC2.
- `Slides/3_19_VolumesEBS.pdf`: visão geral dos volumes EBS.
- `Slides/3_20_TiposVolumesEBS.pdf`: tipos de volumes EBS.
- `Slides/3_21_CriandoVolumeEBS.pdf`: criação de volume EBS.
- `Slides/3_22_AssociandoUmVolumeEBS.pdf`: anexando volume EBS a uma instância.
- `Slides/3_23_IntroducaoSnapshots.pdf`: introdução a snapshots.
- `Slides/3_24_GerenciandoPermissoesSnapshots.pdf`: permissões de snapshots.
- `Slides/3_25_SnapshotLyfeCycle.pdf`: ciclo de vida dos snapshots.
- `Slides/3_26_LixeiraSnapshots.pdf`: lixeira para snapshots.
- `Slides/3_27_ElasticIP.pdf`: Elastic IP.
- `Slides/3_28_IntroducaoSecurityGroups.pdf`: introdução a Security Groups.
- `Slides/3_29_IntroducaoELB.pdf`: introdução ao Elastic Load Balancing.
- `Slides/3_30_CategoriasELB.pdf`: categorias de load balancers.
- `Slides/3_31_LabAndUserData.pdf`: laboratório com `user-data`.
- `Slides/3_32_CriandoTargetsGroups.pdf`: criação de target groups.
- `Slides/3_33_CriandoALB.pdf`: criação de Application Load Balancer.
- `Slides/3_34_ALBResourceMapsAttributes.pdf`: atributos e mapa de recursos do ALB.
- `Slides/3_35_ALBRoteamento.pdf`: roteamento avançado no ALB.
- `Slides/3_36_StickinessTG.pdf`: stickiness em target groups.
- `Slides/3_37_ALBHTTPS.pdf`: configuração de HTTPS no ALB.
- `Slides/3_38_CriandoNGWMySQL.pdf`: laboratório com aplicação e banco.
- `Slides/3_39_IntroducaoAutoScaling.pdf`: introdução ao Auto Scaling.
- `Slides/3_40_CriandoLauchTemplate.pdf`: criação de launch template.
- `Slides/3_41_CriandoScalingGroup.pdf`: criação de Auto Scaling Group.
- `Slides/3_42_AutomaticScaling.pdf`: políticas e conceitos de scaling.
- `Slides/3_43_ASGALB.pdf`: integração entre ASG e ALB.
- `Slides/3_44_InstanceRefresh.pdf`: instance refresh.
- `Slides/3_45_ConsoleToCode.pdf`: Console-to-Code no EC2.
- `Slides/3_46_CloudShell.pdf`: AWS CloudShell.
- `Slides/3_47_EC2InstancesPublic.pdf`: instâncias EC2 públicas.
- `Slides/3_48_EC2SessionManagerAccess.pdf`: acesso via Session Manager.
- `Slides/3_49_EC2SessionManagerAccessSetup.pdf`: configuração do Session Manager.
- `Slides/3_50_EC2InstancesMetadados.pdf`: metadados da instância EC2.
- `Slides/3_51_EC2MetadataProblematica.pdf`: problemas com metadados.
- `Slides/3_52_EC2MetadataFix.pdf`: correções e boas práticas para metadados.
- `Slides/3_53_ConfiguraçõesGlobais.pdf`: configurações globais da seção.
- `Slides/3_54_Final.pdf`: encerramento da seção.
- `Documentos/Links.txt`: links e referências oficiais da seção.
- `Documentos/nginx_amz2-sh.txt`: script de `user-data` para instalar e iniciar Nginx em Amazon Linux 2.

### Arquivos

| Arquivo | Descrição |
|---|---|
| `Slides/3_1_Introducao.pdf` | Introdução ao Amazon EC2. |
| `Slides/3_2_TiposDeInstanciasEC2.pdf` | Tipos de instâncias do EC2. |
| `Slides/3_3_ModelosDeAquisicao.pdf` | Modelos de aquisição de instâncias. |
| `Slides/3_4_ModelosAquisicaoOverviewConsole.pdf` | Visão geral dos modelos de aquisição no console. |
| `Slides/3_6_CicloVidaInstanciasEC2.pdf` | Ciclo de vida das instâncias EC2. |
| `Slides/3_7_ChavesSSH.pdf` | Chaves SSH para acesso seguro. |
| `Slides/3_8_ConectandoEmUmaInstanciaEC2.pdf` | Conexão com instâncias EC2. |
| `Slides/3_9_IntroducaoAMI.pdf` | Introdução às AMIs. |
| `Slides/3_11_CriandoAMI.pdf` | Criação de AMI. |
| `Slides/3_12_CompartilhamentoDeAMI.pdf` | Compartilhamento de AMI. |
| `Slides/3_13_RemovendoAMI.pdf` | Remoção/cancelamento de AMI. |
| `Slides/3_14_IntroducaoEC2ImageBuilder.pdf` | Introdução ao EC2 Image Builder. |
| `Slides/3_15_CriandoBuilderPipeline.pdf` | Pipeline do Image Builder. |
| `Slides/3_16_AWSTags.pdf` | Tags na AWS. |
| `Slides/3_18_ArmazenamentoEC2.pdf` | Armazenamento no EC2. |
| `Slides/3_19_VolumesEBS.pdf` | Visão geral de EBS. |
| `Slides/3_20_TiposVolumesEBS.pdf` | Tipos de volumes EBS. |
| `Slides/3_21_CriandoVolumeEBS.pdf` | Criação de volume EBS. |
| `Slides/3_22_AssociandoUmVolumeEBS.pdf` | Anexando volume EBS. |
| `Slides/3_23_IntroducaoSnapshots.pdf` | Introdução a snapshots. |
| `Slides/3_24_GerenciandoPermissoesSnapshots.pdf` | Permissões de snapshots. |
| `Slides/3_25_SnapshotLyfeCycle.pdf` | Ciclo de vida de snapshot. |
| `Slides/3_26_LixeiraSnapshots.pdf` | Lixeira de snapshots. |
| `Slides/3_27_ElasticIP.pdf` | Elastic IP. |
| `Slides/3_28_IntroducaoSecurityGroups.pdf` | Security Groups. |
| `Slides/3_29_IntroducaoELB.pdf` | Elastic Load Balancing. |
| `Slides/3_30_CategoriasELB.pdf` | Categorias de ELB. |
| `Slides/3_31_LabAndUserData.pdf` | Laboratório com `user-data`. |
| `Slides/3_32_CriandoTargetsGroups.pdf` | Target groups. |
| `Slides/3_33_CriandoALB.pdf` | Application Load Balancer. |
| `Slides/3_34_ALBResourceMapsAttributes.pdf` | Recursos e atributos do ALB. |
| `Slides/3_35_ALBRoteamento.pdf` | Roteamento no ALB. |
| `Slides/3_36_StickinessTG.pdf` | Stickiness em target groups. |
| `Slides/3_37_ALBHTTPS.pdf` | HTTPS no ALB. |
| `Slides/3_38_CriandoNGWMySQL.pdf` | Laboratório com aplicação e MySQL. |
| `Slides/3_39_IntroducaoAutoScaling.pdf` | Introdução ao Auto Scaling. |
| `Slides/3_40_CriandoLauchTemplate.pdf` | Launch template. |
| `Slides/3_41_CriandoScalingGroup.pdf` | Auto Scaling Group. |
| `Slides/3_42_AutomaticScaling.pdf` | Scaling automático. |
| `Slides/3_43_ASGALB.pdf` | Integração ASG + ALB. |
| `Slides/3_44_InstanceRefresh.pdf` | Instance refresh. |
| `Slides/3_45_ConsoleToCode.pdf` | Console-to-Code. |
| `Slides/3_46_CloudShell.pdf` | AWS CloudShell. |
| `Slides/3_47_EC2InstancesPublic.pdf` | Instâncias EC2 públicas. |
| `Slides/3_48_EC2SessionManagerAccess.pdf` | Acesso via Session Manager. |
| `Slides/3_49_EC2SessionManagerAccessSetup.pdf` | Configuração do Session Manager. |
| `Slides/3_50_EC2InstancesMetadados.pdf` | Metadados da instância EC2. |
| `Slides/3_51_EC2MetadataProblematica.pdf` | Problemas com metadados. |
| `Slides/3_52_EC2MetadataFix.pdf` | Correções para metadados. |
| `Slides/3_53_ConfiguraçõesGlobais.pdf` | Configurações globais. |
| `Slides/3_54_Final.pdf` | Encerramento da seção. |
| `Documentos/Links.txt` | Links oficiais e materiais de apoio. |
| `Documentos/nginx_amz2-sh.txt` | Script de `user-data` com Nginx. |

## English

This section covers Amazon EC2 fundamentals, including instance types, purchase models, lifecycle, SSH access, AMIs, Image Builder, tags, EBS storage, snapshots, Elastic IP, Security Groups, Elastic Load Balancing, Auto Scaling, CloudShell, Session Manager, instance metadata, and `user-data`.

### Continuous study text

This section starts with an introduction to Amazon EC2 and then walks through the core concepts needed to use instances effectively and safely. It begins with instance types and purchase models so you can understand how to match capacity and cost to your workload. Next, it covers instance lifecycle, SSH key pairs, and how to connect to Linux servers, building the foundation for remote administration. The section then moves into AMIs, showing how to create, share, and deregister images, and introduces EC2 Image Builder as a way to automate standardized image creation.

For organization and governance, the material explains how to use tags to identify resources and keep environments easier to manage. In storage, it covers EC2 storage, EBS volumes, volume types, volume creation and attachment, and also snapshots, including permissions, lifecycle, and the recycle bin for recovery. The content then moves to Elastic IP and Security Groups, which help control addressing and network access. After that, it focuses on Elastic Load Balancing, especially Application Load Balancer, target groups, routing, stickiness, and HTTPS, plus a `user-data` lab that automates Nginx installation and exposes a sample application.

Finally, the section introduces Auto Scaling, launch templates, Auto Scaling Groups, scaling policies, and ALB integration, showing how to keep applications available and responsive to demand. It also covers Instance Refresh, Console-to-Code, CloudShell, Session Manager access, public instances, instance metadata, common metadata issues, and the global settings that round out day-to-day EC2 usage.

### File summary

- `Slides/3_1_Introducao.pdf`: introduction to Amazon EC2.
- `Slides/3_2_TiposDeInstanciasEC2.pdf`: EC2 instance types.
- `Slides/3_3_ModelosDeAquisicao.pdf`: EC2 purchasing models.
- `Slides/3_4_ModelosAquisicaoOverviewConsole.pdf`: purchasing model overview in the console.
- `Slides/3_6_CicloVidaInstanciasEC2.pdf`: EC2 instance lifecycle.
- `Slides/3_7_ChavesSSH.pdf`: SSH keys for secure access.
- `Slides/3_8_ConectandoEmUmaInstanciaEC2.pdf`: connecting to EC2 instances.
- `Slides/3_9_IntroducaoAMI.pdf`: AMI introduction.
- `Slides/3_11_CriandoAMI.pdf`: creating an AMI.
- `Slides/3_12_CompartilhamentoDeAMI.pdf`: AMI sharing.
- `Slides/3_13_RemovendoAMI.pdf`: AMI deregistration.
- `Slides/3_14_IntroducaoEC2ImageBuilder.pdf`: EC2 Image Builder introduction.
- `Slides/3_15_CriandoBuilderPipeline.pdf`: Image Builder pipeline creation.
- `Slides/3_16_AWSTags.pdf`: AWS tags.
- `Slides/3_18_ArmazenamentoEC2.pdf`: EC2 storage.
- `Slides/3_19_VolumesEBS.pdf`: EBS overview.
- `Slides/3_20_TiposVolumesEBS.pdf`: EBS volume types.
- `Slides/3_21_CriandoVolumeEBS.pdf`: creating an EBS volume.
- `Slides/3_22_AssociandoUmVolumeEBS.pdf`: attaching an EBS volume.
- `Slides/3_23_IntroducaoSnapshots.pdf`: snapshots introduction.
- `Slides/3_24_GerenciandoPermissoesSnapshots.pdf`: snapshot permissions.
- `Slides/3_25_SnapshotLyfeCycle.pdf`: snapshot lifecycle.
- `Slides/3_26_LixeiraSnapshots.pdf`: snapshot recycle bin.
- `Slides/3_27_ElasticIP.pdf`: Elastic IP.
- `Slides/3_28_IntroducaoSecurityGroups.pdf`: Security Groups.
- `Slides/3_29_IntroducaoELB.pdf`: Elastic Load Balancing.
- `Slides/3_30_CategoriasELB.pdf`: ELB categories.
- `Slides/3_31_LabAndUserData.pdf`: `user-data` lab.
- `Slides/3_32_CriandoTargetsGroups.pdf`: target groups.
- `Slides/3_33_CriandoALB.pdf`: Application Load Balancer creation.
- `Slides/3_34_ALBResourceMapsAttributes.pdf`: ALB resources and attributes.
- `Slides/3_35_ALBRoteamento.pdf`: ALB routing.
- `Slides/3_36_StickinessTG.pdf`: target group stickiness.
- `Slides/3_37_ALBHTTPS.pdf`: HTTPS on ALB.
- `Slides/3_38_CriandoNGWMySQL.pdf`: app + MySQL lab.
- `Slides/3_39_IntroducaoAutoScaling.pdf`: Auto Scaling introduction.
- `Slides/3_40_CriandoLauchTemplate.pdf`: launch template.
- `Slides/3_41_CriandoScalingGroup.pdf`: Auto Scaling Group creation.
- `Slides/3_42_AutomaticScaling.pdf`: automatic scaling concepts.
- `Slides/3_43_ASGALB.pdf`: ASG + ALB integration.
- `Slides/3_44_InstanceRefresh.pdf`: instance refresh.
- `Slides/3_45_ConsoleToCode.pdf`: Console-to-Code.
- `Slides/3_46_CloudShell.pdf`: AWS CloudShell.
- `Slides/3_47_EC2InstancesPublic.pdf`: public EC2 instances.
- `Slides/3_48_EC2SessionManagerAccess.pdf`: Session Manager access.
- `Slides/3_49_EC2SessionManagerAccessSetup.pdf`: Session Manager setup.
- `Slides/3_50_EC2InstancesMetadados.pdf`: EC2 instance metadata.
- `Slides/3_51_EC2MetadataProblematica.pdf`: metadata issues.
- `Slides/3_52_EC2MetadataFix.pdf`: metadata fixes and best practices.
- `Slides/3_53_ConfiguraçõesGlobais.pdf`: global settings.
- `Slides/3_54_Final.pdf`: section closing.
- `Documentos/Links.txt`: official links and references.
- `Documentos/nginx_amz2-sh.txt`: `user-data` script to install and start Nginx on Amazon Linux 2.

### Files

| File | Description |
|---|---|
| `Documentos/Links.txt` | Official links and supporting material. |
| `Documentos/nginx_amz2-sh.txt` | `user-data` script with Nginx setup. |
