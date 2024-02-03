# proto file

### doc
- https://grpc-ecosystem.github.io/grpc-gateway/docs/tutorials/
```
go install github.com/grpc-ecosystem/grpc-gateway/v2/protoc-gen-grpc-gateway@latest
go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest
```

### compile proto
```shell
# user.proto
protoc --go_out=. --go-grpc_out=. user.proto
# thor.proto
protoc --go_out=. --go-grpc_out=. thor.proto
# user_data_index.proto
protoc --go_out=. --go-grpc_out=. user_data_index.proto
# service_proxy.proto
protoc --go_out=. --go-grpc_out=. service_proxy.proto
# storage.proto
protoc --go_out=. --go-grpc_out=. storage.proto
```

### How to turn on logging
```shell
export GRPC_GO_LOG_VERBOSITY_LEVEL=99
export GRPC_GO_LOG_SEVERITY_LEVEL=info
```

### proto map (file.proto => project_name)
- user.proto => ares
- user_data_index.proto => web3password-index
- storage.proto => storage