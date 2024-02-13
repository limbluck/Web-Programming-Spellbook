To inject something use ctor
``` C#
public class Service : ICharacterService
{
	private readonly InjectedService _injectedService;
	public CharacterService(InjectedService injectedService)
	{
	    _injectedService = injectedService;
	}
}
```