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
