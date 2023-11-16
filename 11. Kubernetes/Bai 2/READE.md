# Tạo Dockerfile
docker build -t nginx-cafe:v1 -f Dockerfile .

# Push image lên Docker Hub
docker tag nginx-cafe:v1 oogwaymaster/nginx-cafe:v1

# Tạo deployment
kubectl apply -f '.\1. deployment.yaml'

# Chạy service nodePort
kubectl apply -f '.\2. nodePort-service.yaml'