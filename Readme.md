# Readme
A library written in C# to connect [my bot](https://github.com/Not-Storm/Evelin.NET) to A PostgresSQL database

# Dependencies
Dependencies can be installed using dotnet CLI or NuGet Package manager  
The list of the dependencies is as follows
```
Microsoft.EntityFrameworkCore         Version= 5.0.7
Microsoft.EntityFrameworkCore.Tools   Version= 5.0.7
Npgsql                                Version 5.0.7
Npgsql.EntityFrameworkCore.PostgreSQL Version= 5.0.7
StyleCop.Analyzers                    Version= 1.1.118
```

# Environment Variables

The following Environment Variables will be required
```
PostgresSQL_Database     = URL to the database
PostgresSQL_Username     = Username to access database through
PostgresSQL_Password     = Password of the Username used
PostgresSQL_DatabaseName = Name of the database itself
```

# How to use
download the zip or clone the repository to your local machine
```
git clone https://github.com/Not-Storm/DatabaseLibrary.git
```  
Open `.csproj` file of your discord bot add this in it
```
  <ItemGroup>
    <ProjectReference Include=PathToDatabaseProject\DatabaseLibrary\Infrastructure.csproj" />
  </ItemGroup>

```
This is a reference to the database project  
Now add the context and database as a `IServiceCollection` also add reference to the folder by adding to the top `using DatabaseLibrary;`  
```
.AddDbContext<EvelinContext>()
.AddSingleton<Servers>();
```

# License
MIT license  
Free software hellyeah