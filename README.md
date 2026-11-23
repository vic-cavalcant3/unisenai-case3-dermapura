# unisenai-case3-dermapura

LAB11 – Projeto Cloud (DevOps) · Case 3 – DermaPura Cosméticos.

One-page publicada em uma instância **Amazon EC2**, empacotada com **Docker (nginx:alpine)** e implantada automaticamente via **GitHub Actions** a cada push na `main`.

## Arquitetura
`git push` → GitHub Actions (CI: build + teste da imagem) → (CD: SCP + SSH na EC2) → `docker build` / `docker run -p 80:80` → página acessível em `http://54.234.76.175`

## Secrets necessários
| Nome | Valor |
|---|---|
| `EC2_HOST` | IP público da EC2 |
| `EC2_USER` | `ubuntu` |
| `EC2_SSH_KEY` | conteúdo completo da chave `.pem` |

Feito por Evelyn e Victor
