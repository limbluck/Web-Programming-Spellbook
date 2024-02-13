For easier mapping we can use AutoMapper:
1. Instal Microsoft Dependency Injection extension
2. Add AutoMapper package
3. Register AutoMapper
	``` C#
	builder.Services.AddAutoMapper(typeof(Program).Assembly);
	```
4. Inject AutoMapper
	``` C#
	private readonly IMapper _mapper;
	public CharacterService(IMapper mapper)
	{
	    _mapper = mapper;
	}
	```
5. Create an automapper profile
	``` C#
	public class AutoMapperProfile : Profile
	{
	    public AutoMapperProfile()
	    {
	        CreateMap<OldDatatType1, NewDatatType1>();
	        CreateMap<OldDatatType2, NewDatatType2>();
	    }
	}
	```
1. Map an object
	``` C#
	// For a single entity:
	var newObject = _mapper.Map<NewDataType>(oldObject);
	// For a list:
	var newList = oldList.Select(c => _mapper.Map<NewDataType>(c)).ToList();
	```
