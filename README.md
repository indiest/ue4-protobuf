### What is this?

This is an Unreal Engine 4 plugin that integrates [Protobuf](https://github.com/protocolbuffers/protobuf) into the project without requiring you to add system PATH or anything else.

### How do use?

1. add the plugin to the project and enable it.
2. add the following property to `build.cs` of modules :

```csharp
PublicDependencyModuleNames.Add("Protobuf");
```

4. Create `.proto` file into project source code folder 
5. Launch the Project in Editor, Click the `Protoc` button.

### Protobuf Version

- Protobuf v3.21.5
- Protobuf v3.5.1
### Upgrade Protobuf
For protobuf v3.21.x
1. Use [adapte script](https://github.com/metaworking/adapt-protobuf-to-ue) to convert protobuf source
2. Copy the conversion result to `Source/Protobuf/ThirdParty/google`
3. Compile `Protoc.exe` of same version, you can refer to [UE4Protobuf](https://gitee.com/love_linger/UE4Protobuf). We just want to add some `warning(disable: xxxx)` to .pb.h and .pb.cpp files when generating them
4. Copy the `Protoc.exe` to `Source/Protobuf/ThirdParty/bin`