# ginLite
最小化gin，删除了不常用的代码，方便学习
## 使用方式
`go get -u zhang00829/ginLite`
## 快速使用
``` go 

import gin "github.com/zhang00829/ginLite"

func main() {
	r := gin.Default()
	r.GET("/ping", func(c *gin.Context) {
		c.JSON(200, gin.H{
			"message": "pong",
		})
	})
	r.Run(":8099")
}

```
## 简化后的结构
```text
.
├── README.md
├── binding
│   ├── binding.go
│   ├── default_validator.go
│   ├── form.go
│   ├── form_mapping.go
│   ├── header.go
│   ├── json.go
│   ├── multipart_form_mapping.go
│   ├── query.go
│   └── uri.go
├── context.go
├── errors.go
├── fs.go
├── gin.go
├── go.mod
├── go.sum
├── internal
│   ├── bytesconv
│   │   └── bytesconv.go
│   └── json
│       └── json.go
├── logger.go
├── mode.go
├── path.go
├── recovery.go
├── render
│   ├── json.go
│   └── render.go
├── response_writer.go
├── routergroup.go
├── tree.go
└── utils.go
```