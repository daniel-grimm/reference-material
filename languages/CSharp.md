# C#
C# is a language developed and maintained by Microsoft. It's often used in conjunction with the .NET platform also created and maintained by Microsoft.

# ASP.NET Core MVC
ASP.NET Core MVC has become the standard way to make APIs using C# and .NET. Using the controllers as REST endpoints, it is flexible to most architectural patterns.

## Example Controller
```csharp
using System;

namespace Example;

[ApiController]
[Route("users")]
[Authorize("read:users")]
class UserController : ControllerBase
{
    private ILogger<UserController> Logger { get; }

    public UserController(
        ILogger<UserController> logger
    )
    {
        Logger = logger;
    }

    [HttpGet]
    [Route("")]
    [ProducesResponseType(statusCode: StatusCodes.Status200OK)]
    [Consumes(MediaTypeNames.Application.Json)]
    [Description("Gets all users")]
    public async Task<IActionResult> GetAllUsers()
    {
        Logger.LogInformation("{Controller}: This is structured logging.", nameof(UserController));

        return Ok();
    }
}
```
