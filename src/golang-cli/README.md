# 출처
https://dev.to/aurelievache/learning-go-by-examples-part-3-create-a-cli-app-in-go-1h43


```
go get -u github.com/spf13/cobra@latest
```

```
go install github.com/spf13/cobra-cli@latest
```

```
echo "export PATH=$PATH:$(go env GOPATH)/bin" >> ~/.zshrc
source ~/.zshrc
```

```
☁  golang-cli [main] ⚡  cobra-cli init
Your Cobra application is ready at
/home/sangylee/project/golang-playground/src/golang-cli
```

```
go get github.com/spf13/viper@v1.8.1
```

```
# get command를 cil에 추가
cobra-cli add get
```

```
같은 package면 파일 달라도 변수 공유됨
Cobra는 이 패턴으로 명령 연결함
```


# struct literal
```
// getCmd represents the get command
var getCmd = &cobra.Command{
	Use:   "get",
	Short: "A brief description of your command",
	Long: `A longer description that spans multiple lines and likely contains examples
and usage of using your command. For example:

Cobra is a CLI library for Go that empowers applications.
This application is a tool to generate the needed files
to quickly create a Cobra application.`,
	Run: func(cmd *cobra.Command, args []string) {
		fmt.Println("get called")
	},
}
```

구조체 만들면서 값 넣기