# Architecture — CyberThreat Atlas

```mermaid
flowchart TB
 S[Sources] --> I[Ingestion]
 I --> N[Normalization]
 N --> P[Provenance]
 P --> A[Atlas Store]
 A --> IOC[IOC]
 A --> TTP[TTP]
 A --> CAM[Campaigns]
 A --> API[Search / API]
 API --> D[Defenders / Researchers]
 D --> F[Feedback]
 F --> A
```

## Principes

Chaque élément doit conserver provenance, date, niveau de confiance et contexte. Les données sensibles doivent être filtrées avant publication. L'objectif est d'améliorer la défense, pas de faciliter l'abus.