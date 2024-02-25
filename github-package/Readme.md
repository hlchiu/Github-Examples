export GH_USERNAME='hlchiu'
export GH_TOKEN=''
export GH_IMAGE_NAME='h-world'
export GH_VER=1.0.0
export TAG_NAME="ghcr.io/$GH_USERNAE/$IMAGE_NAME:$GH_VER"

echo $GH_TOKEN | docker login ghcr.io -u $GH_USERNAME --password-stdin
/home/codespace/.docker/config.json.

docker tag h-world:latest $TAG_NAME
docker push $TAG_NAME

LABEL org.opencontainers.image.source https://github.com/OWNER/REPO
