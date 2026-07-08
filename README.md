# TechX App

`techx-app` chứa source ứng dụng chính của TechX Corp online store: nhiều microservice, web storefront, cart/checkout/payment, Kafka pipeline, AI product-review summarizer và observability config dùng cho local.

## Layout

| Đường dẫn | Vai trò |
| --- | --- |
| `src/` | Application microservices, AI review service, mock LLM, observability config. |
| `docker-compose.yml` | Build/chạy local và là nguồn để CI build image. |
| `docker-compose.minimal.yml` | Chạy local bản tối thiểu. |
| `docker-compose-tests.yml` | Chạy test bằng Docker Compose. |
| `Makefile` | Helper build/proto/buildx từ source gốc. |
| `.github/workflows/app-ci.yml` | CI kiểm tra app. |
| `.github/workflows/image-build-push.yml` | Build image và push lên ECR. |

## Run Locally

```powershell
docker compose --env-file .env --env-file .env.override -f docker-compose.yml up --force-recreate --remove-orphans --detach
```

Storefront:

```text
http://localhost:8080/
```

## Kubernetes Deploy

Không deploy Kubernetes trực tiếp từ folder này. Luồng chuẩn nằm ở:

```text
../techx-gitops/charts/techx-corp
../techx-gitops/environments/base
```

Hướng dẫn đầy đủ:

```text
../docs/deployment/STEP_BY_STEP_BEST_PRACTICE.md
```

## License

Distributed under the Apache License 2.0. See `LICENSE`.
