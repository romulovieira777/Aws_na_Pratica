# Seção 06 — Amazon S3

Documentação da seção de Amazon S3 do curso **AWS na Prática**.

## Português (Brasil)

Esta seção aborda os fundamentos de armazenamento em nuvem com o Amazon S3, incluindo buckets, classes de armazenamento, criptografia, versionamento, ciclo de vida, replicação, controle de acesso, políticas de bucket, hosting estático, URLs pré-assinadas, logs de acesso e aceleração de transferência.

### Texto corrido para estudo

Nesta seção, o estudo começa com a introdução ao Amazon S3, o serviço de armazenamento de objetos da AWS. O conteúdo explica o conceito de buckets, a organização lógica dos dados e a importância de entender a nomenclatura e as melhores práticas de criação de containers no S3. Em seguida, a seção apresenta as classes de armazenamento, mostrando como cada uma foi pensada para equilíbrio entre custo, desempenho e durabilidade, conforme o tipo de dado e o padrão de acesso.

A parte seguinte trata da segurança e do gerenciamento de dados. O material cobre criptografia, versionamento de objetos e lifecycle policies, que permitem automatizar transições entre classes e expiração de arquivos. Também é apresentado o tema de replicação entre regiões, útil para durabilidade, recuperação de desastres e otimização de acesso. Depois, entra no controle de acesso, com ACLs, bucket policies e políticas condicionais, além de reforçar o uso de Block Public Access para evitar exposição indevida de dados.

O conteúdo segue com hosting estático em S3, demonstrando como hospedar sites simples de forma prática e eficiente. Também são abordados URLs pré-assinadas, que permitem acesso temporário e seguro a objetos, e logs de acesso do S3 para rastrear solicitações e entender como os dados estão sendo consumidos. Os materiais fecham com transfer acceleration, integração com arquivos em EC2 e uma visão geral de como o S3 pode ser usado em cenários reais de armazenamento, compartilhamento e automação.

### Resumo dos arquivos

- `Slides/6_1_Introducao.pdf`: introdução ao Amazon S3.
- `Slides/6_2_BucketsVectoreTable.pdf`: buckets e conceitos de armazenamento em tabela/vetor.
- `Slides/6_3_ClassesDeArmazenamento.pdf`: classes de armazenamento do S3.
- `Slides/6_4_Criptografia.pdf`: criptografia no Amazon S3.
- `Slides/6_5_CriandoBucketENomenclatura.pdf`: criação de buckets e boas práticas de nomenclatura.
- `Slides/6_6_CriandoBucketDirectory.pdf`: criação de buckets de diretório.
- `Slides/6_7_RemovendoBuckets.pdf`: remoção de buckets.
- `Slides/6_8_UploadObject.pdf`: upload de objetos no S3.
- `Slides/6_8_VersionamentoObjetos.pdf`: versionamento de objetos.
- `Slides/6_9_HabilitandoVersionamento.pdf`: habilitação do versionamento.
- `Slides/6_10_S3LifecyclePolicy.pdf`: políticas de ciclo de vida.
- `Slides/6_11_S3LifecycleSetup.pdf`: configuração de lifecycle no bucket.
- `Slides/6_12_ReplicacaoObjetos.pdf`: replicação de objetos.
- `Slides/6_14_GerenciamentoAcessos.pdf`: gerenciamento de acessos.
- `Slides/6_15_TrabalhandoComACL.pdf`: ACLs no S3.
- `Slides/6_16_PoliticasBuckets.pdf`: políticas de bucket.
- `Slides/6_17_BucketPolicySample1.pdf`: exemplos de bucket policies.
- `Slides/6_19_PolicyEditor.pdf`: editor de políticas.
- `Slides/6_21_Conditionals.pdf`: condições e expressões em políticas.
- `Slides/6_22_ForceBlockPublicAccess.pdf`: bloqueio de acesso público.
- `Slides/6_23_WebHosting.pdf`: hosting estático com S3.
- `Slides/6_24_URLPreAssinada.pdf`: URLs pré-assinadas.
- `Slides/6_25_AccessLogs.pdf`: logs de acesso no S3.
- `Slides/6_26_AccessLogsSetup.pdf`: configuração de logs de acesso.
- `Slides/6_26_S3Files.pdf`: uso de arquivos e objetos no S3.
- `Slides/6_27_TransferAccelerate.pdf`: Amazon S3 Transfer Acceleration.
- `Slides/S3Files_howto_s3_files_ec2.pdf`: integração de arquivos S3 com EC2.
- `Links/Links.txt`: links e referências oficiais da seção.

### Arquivos

| Arquivo | Descrição |
|---|---|
| `Slides/6_1_Introducao.pdf` | Introdução ao Amazon S3. |
| `Slides/6_2_BucketsVectoreTable.pdf` | Conceitos de buckets e estruturas de armazenamento. |
| `Slides/6_3_ClassesDeArmazenamento.pdf` | Classes de armazenamento do S3. |
| `Slides/6_4_Criptografia.pdf` | Criptografia do Amazon S3. |
| `Slides/6_5_CriandoBucketENomenclatura.pdf` | Criação e nomenclatura de buckets. |
| `Slides/6_6_CriandoBucketDirectory.pdf` | Buckets de diretório. |
| `Slides/6_7_RemovendoBuckets.pdf` | Remoção de buckets. |
| `Slides/6_8_UploadObject.pdf` | Upload de objetos. |
| `Slides/6_8_VersionamentoObjetos.pdf` | Versionamento de objetos. |
| `Slides/6_9_HabilitandoVersionamento.pdf` | Habilitação do versionamento. |
| `Slides/6_10_S3LifecyclePolicy.pdf` | Política de lifecycle do S3. |
| `Slides/6_11_S3LifecycleSetup.pdf` | Configuração de lifecycle. |
| `Slides/6_12_ReplicacaoObjetos.pdf` | Replicação de objetos. |
| `Slides/6_14_GerenciamentoAcessos.pdf` | Gestão de acessos no S3. |
| `Slides/6_15_TrabalhandoComACL.pdf` | ACLs na AWS. |
| `Slides/6_16_PoliticasBuckets.pdf` | Políticas de bucket. |
| `Slides/6_17_BucketPolicySample1.pdf` | Exemplos de bucket policies. |
| `Slides/6_19_PolicyEditor.pdf` | Editor de políticas. |
| `Slides/6_21_Conditionals.pdf` | Condições em políticas. |
| `Slides/6_22_ForceBlockPublicAccess.pdf` | Bloqueio de acesso público. |
| `Slides/6_23_WebHosting.pdf` | Hosting estático em S3. |
| `Slides/6_24_URLPreAssinada.pdf` | URLs pré-assinadas. |
| `Slides/6_25_AccessLogs.pdf` | Logs de acesso do S3. |
| `Slides/6_26_AccessLogsSetup.pdf` | Configuração de logs de acesso. |
| `Slides/6_26_S3Files.pdf` | Gerenciamento de arquivos S3. |
| `Slides/6_27_TransferAccelerate.pdf` | S3 Transfer Acceleration. |
| `Slides/S3Files_howto_s3_files_ec2.pdf` | Arquivos S3 em integração com EC2. |
| `Links/Links.txt` | Referências oficiais e materiais de apoio. |

## English

This section covers Amazon S3 storage fundamentals, including buckets, storage classes, encryption, versioning, lifecycle management, replication, access control, bucket policies, static website hosting, presigned URLs, access logs, and transfer acceleration.

### Continuous study text

This section begins with an introduction to Amazon S3, AWS's object storage service. The material explains the concept of buckets, logical data organization, and the importance of proper bucket naming and best practices for creating S3 containers. It then moves into storage classes, showing how each class balances cost, performance, and durability depending on the workload and access pattern.

The next part focuses on security and data management. It covers encryption, object versioning, and lifecycle policies that automate transitions between storage classes and object expiration. The section also introduces replication across regions, which is useful for durability, disaster recovery, and access optimization. After that, it explores access control with ACLs, bucket policies, and conditional policies, reinforcing the use of Block Public Access to prevent accidental exposure of data.

The content continues with static website hosting on S3, demonstrating how to host simple websites efficiently and economically. It also addresses presigned URLs for secure temporary access, plus server access logs to track requests and understand how data is being consumed. The materials conclude with transfer acceleration, file handling, and real-world patterns for using S3 in EC2 and automation scenarios.

### File summary

- `Slides/6_1_Introducao.pdf`: introduction to Amazon S3.
- `Slides/6_2_BucketsVectoreTable.pdf`: buckets and storage structures.
- `Slides/6_3_ClassesDeArmazenamento.pdf`: S3 storage classes.
- `Slides/6_4_Criptografia.pdf`: S3 encryption.
- `Slides/6_5_CriandoBucketENomenclatura.pdf`: bucket creation and naming best practices.
- `Slides/6_6_CriandoBucketDirectory.pdf`: directory buckets.
- `Slides/6_7_RemovendoBuckets.pdf`: bucket deletion.
- `Slides/6_8_UploadObject.pdf`: object upload.
- `Slides/6_8_VersionamentoObjetos.pdf`: object versioning.
- `Slides/6_9_HabilitandoVersionamento.pdf`: enabling versioning.
- `Slides/6_10_S3LifecyclePolicy.pdf`: S3 lifecycle policies.
- `Slides/6_11_S3LifecycleSetup.pdf`: lifecycle configuration.
- `Slides/6_12_ReplicacaoObjetos.pdf`: object replication.
- `Slides/6_14_GerenciamentoAcessos.pdf`: access management in S3.
- `Slides/6_15_TrabalhandoComACL.pdf`: ACLs in S3.
- `Slides/6_16_PoliticasBuckets.pdf`: bucket policies.
- `Slides/6_17_BucketPolicySample1.pdf`: bucket policy examples.
- `Slides/6_19_PolicyEditor.pdf`: policy editor.
- `Slides/6_21_Conditionals.pdf`: policy conditions.
- `Slides/6_22_ForceBlockPublicAccess.pdf`: public access blocking.
- `Slides/6_23_WebHosting.pdf`: static website hosting.
- `Slides/6_24_URLPreAssinada.pdf`: presigned URLs.
- `Slides/6_25_AccessLogs.pdf`: S3 access logs.
- `Slides/6_26_AccessLogsSetup.pdf`: configuring access logging.
- `Slides/6_26_S3Files.pdf`: managing files in S3.
- `Slides/6_27_TransferAccelerate.pdf`: Amazon S3 Transfer Acceleration.
- `Slides/S3Files_howto_s3_files_ec2.pdf`: S3 file usage with EC2.
- `Links/Links.txt`: official references and support material.

### Files

| File | Description |
|---|---|
| `Slides/6_1_Introducao.pdf` | Introduction to Amazon S3. |
| `Slides/6_2_BucketsVectoreTable.pdf` | Buckets and storage concepts. |
| `Slides/6_3_ClassesDeArmazenamento.pdf` | S3 storage classes. |
| `Slides/6_4_Criptografia.pdf` | S3 encryption. |
| `Slides/6_5_CriandoBucketENomenclatura.pdf` | Bucket creation and naming. |
| `Slides/6_6_CriandoBucketDirectory.pdf` | Directory bucket concepts. |
| `Slides/6_7_RemovendoBuckets.pdf` | Bucket removal. |
| `Slides/6_8_UploadObject.pdf` | Object upload. |
| `Slides/6_8_VersionamentoObjetos.pdf` | Object versioning. |
| `Slides/6_9_HabilitandoVersionamento.pdf` | Enabling versioning. |
| `Slides/6_10_S3LifecyclePolicy.pdf` | Lifecycle policies. |
| `Slides/6_11_S3LifecycleSetup.pdf` | Lifecycle configuration. |
| `Slides/6_12_ReplicacaoObjetos.pdf` | Object replication. |
| `Slides/6_14_GerenciamentoAcessos.pdf` | Access management in S3. |
| `Slides/6_15_TrabalhandoComACL.pdf` | ACLs in AWS. |
| `Slides/6_16_PoliticasBuckets.pdf` | Bucket policies. |
| `Slides/6_17_BucketPolicySample1.pdf` | Bucket policy examples. |
| `Slides/6_19_PolicyEditor.pdf` | Policy editor. |
| `Slides/6_21_Conditionals.pdf` | Conditions in policies. |
| `Slides/6_22_ForceBlockPublicAccess.pdf` | Public access blocking. |
| `Slides/6_23_WebHosting.pdf` | Static website hosting. |
| `Slides/6_24_URLPreAssinada.pdf` | Presigned URLs. |
| `Slides/6_25_AccessLogs.pdf` | S3 access logs. |
| `Slides/6_26_AccessLogsSetup.pdf` | Configuring access logs. |
| `Slides/6_26_S3Files.pdf` | S3 file management. |
| `Slides/6_27_TransferAccelerate.pdf` | S3 Transfer Acceleration. |
| `Slides/S3Files_howto_s3_files_ec2.pdf` | S3 file usage with EC2. |
| `Links/Links.txt` | Official references and support material. |
