### Resumo
Gerando os Models de um projeto ASP.NET Core MVC baseados em um banco pré-existente

### Criando um projeto MVC
```
dotnet new mvc -au None
```

### Instalação de um provedor
Consulte o [provedor de acesso] para o seu tipo de banco de dados. 

Para este exemplo, usaremos o do MySql e SQL Server

***MySql***
```sh
Install-Package Pomelo.EntityFrameworkCore.MySql -Version 2.1.2
```
***SqlServer***
Não é necessario fazer instalações adicionais para o SQL Server, uma vez que o proveder para o EF esta dentro deo Microsoft.AspnetCore.App

### Scarffold
***MySql***
```
Scaffold-DbContext "Server=NomeDoServidor;Database=NomeDoBanco;Uid=NomeDoUsuario;Pwd=SenhaDoUsuario;" Pomelo.EntityFrameworkCore.MySql -OutputDir Models

```

***SqlServer***
```
Scaffold-DbContext "Server=(localdb)\mssqllocaldb;Database=NomeDoBanco;Trusted_Connection=True;" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models
```

 [provedor de acesso]: <https://docs.microsoft.com/pt-br/ef/core/providers/index>
 
