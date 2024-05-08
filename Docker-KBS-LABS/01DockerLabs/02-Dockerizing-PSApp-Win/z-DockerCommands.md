# Build the docker image from the docker file

docker image build --tag sunsivadocker/my-ps-app:win01 .

# run the image as contain
docker run sunsivadocker/my-ps-app:win01

# push the image to docker hub registry
docker push sunsivadocker/my-ps-app:win01

# build the long-run image
docker image build --tag sunsivadocker/my-ps-app:win01-longrun
# run the image as container
dcoker run sunsivadocker/my-ps-app:win01-longrun

docker container ls

docker exec -t <containerid> "powershell" or "cmd"