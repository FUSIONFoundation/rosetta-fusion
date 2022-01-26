make build-local

docker run -d --rm --ulimit "nofile=100000:100000" -v "$(pwd)/fusion-data:/data" -e "MODE=ONLINE" -e "NETWORK=MAINNET" -e "PORT=8080" -p 8080:8080 -p 40408:40408 rosetta-fusion:latest
