# Presentación en linea de las clases de PostgreSQL

>[!NOTE]
> Usando como librería: [reveal.js-plugins](https://github.com/rajgoel/reveal.js-plugins)

>[!WARNING]
> Advertencia

>[!TIP]
> Tips

>[!IMPORTANT]
> Importante

>[!CAUTION]
> Precaución

```mermaid
erDiagram
    CUSTOMER }|..|{ DELIVERY-ADDRESS : has
    CUSTOMER ||--o{ ORDER : places
    CUSTOMER ||--o{ INVOICE : "liable for"
    DELIVERY-ADDRESS ||--o{ ORDER : receives
    INVOICE ||--|{ ORDER : covers
    ORDER ||--|{ ORDER-ITEM : includes
    PRODUCT-CATEGORY ||--|{ PRODUCT : contains
    PRODUCT ||--o{ ORDER-ITEM : "ordered in"
```
