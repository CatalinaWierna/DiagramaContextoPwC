```mermaid
C4Context
    title Diagrama de Contexto de Sistema (Nivel 1) - Ecosistema Digital Global de PwC

    %% Actores / Personas
    Person(cliente, "Cliente Corporativo", "Directivos, gerentes financieros y auditados de las empresas que contratan a PwC.")
    Person(consultor, "Profesional de PwC", "Socios, consultores, auditores y especialistas en impuestos de la red global.")
    Person(regulador, "Entidad Regulatoria", "Gobiernos, agencias tributarias y comisiones de valores (ej. SEC, AFIP, IRS).")

    %% Sistema Principal
    System(pwc_system, "Plataforma Global de Servicios PwC", "El ecosistema central de software que consolida auditoría, consultoría, impuestos e inteligencia de negocios de forma segura.")

    %% Sistemas Externos
    System_Ext(erp_cliente, "Sistemas del Cliente (ERP/CRM)", "Infraestructura on-premise o cloud del cliente (SAP, Oracle, Salesforce) de donde se extrae la data.")
    System_Ext(market_data, "Proveedores de Mercado", "Fuentes de inteligencia financiera e industrial (Bloomberg, Reuters, S&P).")
    System_Ext(gov_system, "Sistemas Gubernamentales", "Portales y APIs de entidades fiscales para cruce de datos y presentaciones.")
    System_Ext(tech_partners, "Cloud & Tech Partners", "Infraestructura y servicios de aliados estratégicos (AWS, Microsoft Azure, Google Cloud).")

    %% Relaciones
    Rel(cliente, pwc_system, "Solicita servicios, sube documentación confidencial, aprueba y descarga informes", "Portal Web / HTTPS")
    Rel(consultor, pwc_system, "Procesa datos masivos, gestiona proyectos, colabora y genera entregables", "Intranet / SSO")
    Rel(regulador, pwc_system, "Recibe auditorías y presentaciones de cumplimiento normativo", "Canales Seguros / B2B")

    Rel(pwc_system, erp_cliente, "Extrae información contable, operativa y financiera", "ETL / APIs Seguras")
    Rel(pwc_system, market_data, "Consume tendencias macroeconómicas y benchmarks", "REST APIs")
    Rel(pwc_system, gov_system, "Automatiza declaraciones y valida cumplimiento fiscal", "APIs / SFTP")
    Rel(pwc_system, tech_partners, "Delega procesamiento pesado, almacenamiento y modelos de IA", "Cloud Networking")
```
