## Todo 

- Jenkins Research

```mermaid
graph TD;
    A[Developer Push to GitHub] -->|Triggers| B[Jenkins Build];
    B --> C[Jenkins Test];
    C -->|Deploy to Production Server| D[Deploy - Master Branch];
    C -->|Deploy to Dev Server| E[Deploy - Dev Branch];
```

