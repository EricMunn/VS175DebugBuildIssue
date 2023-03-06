MRE for VS Debug/Build issue with VS 2022 17.5

https://developercommunity.visualstudio.com/t/VS-2022-175-no-longer-honors-CopyToOutp/10297917

Fails with all combinations of 
 - `<Content>`
 - `<None>`
 - `<CopyToOutputDirectory>Always</CopyToOutputDirectory>`
 - `<CopyToOutputDirectory>PreserveNewest</CopyToOutputDirectory>`

 ```xml
   <ItemGroup>
    <None Include="foobar.txt">
      <CopyToOutputDirectory>Always</CopyToOutputDirectory>
    </None>
  </ItemGroup>
```
```xml
   <ItemGroup>
    <Content Include="foobar.txt">
      <CopyToOutputDirectory>Always</CopyToOutputDirectory>
    </Content>
  </ItemGroup>
```
```xml
   <ItemGroup>
    <None Include="foobar.txt">
      <CopyToOutputDirectory>PreserveNewest</CopyToOutputDirectory>
    </None>
  </ItemGroup>
```

```xml
   <ItemGroup>
    <Content Include="foobar.txt">
      <CopyToOutputDirectory>PreserveNewest</CopyToOutputDirectory>
    </Content>
  </ItemGroup>
```
