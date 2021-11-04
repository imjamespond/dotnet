# Init
`dotnet new -l` or `dotnet new` 列出模板  
`dotnet new mvc -o some-project` mvc项目  
`dotnet new console -o test-dll` dll项目  
`dotnet build`
# Invoke Dll  
修改 test-mvc.csproj
```
  <ItemGroup>
    <Reference Include="test-dll">
      <HintPath>dll\test-dll.dll</HintPath>
    </Reference>
  </ItemGroup>
```
cs中引
```
using Foobar;
...
Foo.SayHelloTo("someone")
```
