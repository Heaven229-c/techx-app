# Scripts

Thư mục này dành cho script phụ trợ của repo app.

Luồng build/push image chuẩn hiện tại nằm trong:

```text
.github/workflows/image-build-push.yml
```

Script cũ từ folder `deploy/build-push-images.sh` đã được lưu tại:

```text
../docs/mentor-source/deploy/build-push-images.sh
```

Script cũ đó push lên Docker Hub và phù hợp tham khảo local/manual hơn là luồng enterprise. Với dự án chuẩn CDO03, image được build bằng GitHub Actions và push lên AWS ECR.
