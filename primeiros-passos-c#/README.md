![Primeiros passos com .NET + C#](http://matheusti.com.br/my-github-images/bootcamp-dio-localizaLabs/primeiros-passos-c#/primeiros-passos-c#.png)

## Aula 1
É aborado um pouco da história do .NET e onde usar .NET.

## Aula 2 
### **Preparação do ambiente**
Na aula é demonstrado a como configurar o ambiente para .NET 3 direto do site da Microsoft, eu estarei utilizando o Docker para criar o meu ambiente de desenvolvimento. Atualmente o .NET está na versão 5, porém para seguir com o mesmo ambiente de deselvomvimento demostrado em aula, seguirei com o .NET 3.1
 - **.NET SDK** Indicado para uso em desenvolvimento
 - **.NET Runtime** Indicado para uso em produção

#### Docker
> Obtendo a imagem do .NET 3.1 SDK
```docker
docker pull mcr.microsoft.com/dotnet/sdk:3.1
```

Agora precisamos navegar até a pasta onde vai conter os exercícios, no meu caso é a pasta `C:\Dev\GitHub\bootcamp-dio-localizaLabs\primeiros-passos-c#\`
```
cd C:\Dev\GitHub\bootcamp-dio-localizaLabs\primeiros-passos-c#\
```
É interessante ficar um nível antes da pasta final pois a pasta final será concatenada no comando do docker.
> Inicializando o container
- Windows via Prompt de comando
    ```docker
    docker run -it --rm --name NOME_DO_CONTAINER -v %CD%/src:/src ID_DA_IMAGEM
    ```
- Linux/Mac ou Windows via PowerShell
    ```docker
    docker run -it --rm --name NOME_DO_CONTAINER -v ${PWD}/src:/src ID_DA_IMAGEM
    ```
O comando acima cria o container e após o uso do container ele é removido. Após baixar a imagem, você pode encontrar o ID da imagem com o seguinte comando:
```docker
docker images -a
```
### **Conhecendo a CLI**
|              |            |
|:-------------:      |:-------------:|
| `dotnet --version`  | Exibe a versão instalada.
| `dotnet --help`     | Exibe uma documentação mais detalhada online para o comando especificado.|
| `dotnet --info` | informações detalhadas sobre uma instalação do .NET e o ambiente do computador. |
| `dotnet build` | Compila um projeto e todas as suas dependências.|
| `dotnet nuget` | Gerenciador de pacotes.|
| `dotnet new` | Cria um novo projeto, arquivo de configuração ou solução com base no modelo especificado.|
| `dotnet restore` | Restaura as dependências e as ferramentas de um projeto.|
| `dotnet run` | Executa o código-fonte sem qualquer comando de compilação ou inicialização explícito.|

### Criando uma aplicação console

```csharp
dotnet new console -n NOME_DA_APLICAÇÃO
```

### Executando a aplicação
#### Com a pasta do projeto aberta
```csharp
dotnet run
```
É necessário navegar até a pasta /NOME_DA_APLICAÇÃO, pois o comando ```run``` precisa de um arquivo ```.csproj```, arquivo esse que fica na pasta do projeto que foi criado.

#### Fora da pasta do projeto
```csharp
dotnet run -p CAMINHO_DA_PASTA
```