# C#

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