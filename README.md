# auftrag_3_2

export CR_PAT=<Github_Token>

echo $CR_PAT | docker login ghcr.io -u <githubusername> --password-stdin

export DOCKER_DEFAULT_PLATFORM=linux/amd64

docker pull nginx:latest --platform linux/amd64

docker tag nginx:latest ghcr.io/benschwarz1982/nginx:v1

docker build . -t ghcr.io/benschwarz1982/nginx:v1

docker push ghcr.io/benschwarz1982/nginx:v1

docker run -it --rm -d -p 8080:80 --name auftrag_3_2 ghcr.io/benschwarz1982/nginx:v1
