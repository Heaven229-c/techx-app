# TechX App Repo Role

Repo này là `techx-app`.

Nó chứa source app thật của mentor sau khi đã đưa vào cấu trúc chuẩn hiện tại.

Trách nhiệm:

- Build và test application source.
- Build Docker image cho từng service.
- Push image lên ECR theo tag `sha-<commit>-<service>`.
- Không chứa Terraform.
- Không trực tiếp quản lý trạng thái deploy Kubernetes.

CI/CD chính:

```text
.github/workflows/app-ci.yml
.github/workflows/image-build-push.yml
```
