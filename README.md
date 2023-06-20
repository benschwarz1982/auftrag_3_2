# auftrag_3_2

docker pull nginx:latest --platform linux/amd64

docker tag nginx:latest ghcr.io/benschwarz1982/nginx:v1

docker build . -t ghcr.io/benschwarz1982/nginx:v1

docker push ghcr.io/benschwarz1982/nginx:v1

docker run -it --rm -d -p 8080:80 --name auftrag_3_2 ghcr.io/benschwarz1982/nginx:v1