[[Golang]]
go run main.go
Создается временный бинарник в оперативной памяти, программа выполняется

Если же вы хотите скомпилировать программу, то-есть получить готовый бинарник для запуска на машинах без Go (для windows это будет .exe) - выполните следующую команду:
go build main.go
go build -o main.bin main.go


cd C:\Users\admin\GolandProjects
go run main.go
—Hello world!
C:\Users\admin\GolandProjects>go build -o trtr.bin main.go
C:\Users\admin\GolandProjects>trtr.bin
—Hello world!

cd C:\Users\admin\GolandProjects
mkdir TestProject
cd TestProject
go mod init test
—go: creating new go.mod: module test
go mod tidy
go run main.go
—Hello warld
go build -o main.bin main.go
main.bin
—Hello warld