# APS.NET Core Identity with MySQL

Application in ASP.NET Core 2.0 with Identity using a MySQL Database.

## Prerequisites

To make this works you need to install
* [Pomelo.EntityFrameworkCore.MySql](https://www.nuget.org/packages/Pomelo.EntityFrameworkCore.MySql) - Plugin to allow Identity use a MySQL Database

### How to use

After install Pomelo, enable Identity to use MySQL in the method ConfigureServices of your class Startup.cs.

```
public void ConfigureServices(IServiceCollection services)
{
    services.AddDbContext<ApplicationDbContext>(options =>
        options.UseMySql(Configuration.GetConnectionString("IdentityConnection")));

    (... another stuff)
}
```
