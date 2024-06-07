# google-authenticator
## 注意事项
时间戳一要相同

## 本人用途
jumpserver的多因子认证

## 使用
```bash
# 请将xxx 替换为自己密钥
./google-authenticator -secret xxx
# 或者 设置secret 为环境变量
# linux and mac export google_auth_secret=xxx
./google-authenticator
```

## 编译
```bash
# Linux 下编译 Mac 和 Windows 64位可执行程序
CGO_ENABLED=0 GOOS=darwin GOARCH=amd64 go build main.go
CGO_ENABLED=0 GOOS=windows GOARCH=amd64 go build main.go

# Mac 下编译 Linux 和 Windows 64位可执行程序
CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build main.go
CGO_ENABLED=0 GOOS=windows GOARCH=amd64 go build main.go
```

```powershell
# Windows 下编译 Mac 和 Linux 64位
SET CGO_ENABLED=0
SET GOOS=darwin
SET GOARCH=amd64
go build main.go

SET CGO_ENABLED=0
SET GOOS=linux
SET GOARCH=amd64
go build main.go
```