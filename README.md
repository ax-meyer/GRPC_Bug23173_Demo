# GRPC_Bug23173_Demo
Demonstration of GRPC issue 23173 https://github.com/grpc/grpc/issues/23173

## Whats happening?
5 Projects in the solution:
* StandaloneProtoCompilation - .netCore 3.1 Console App, compiling protobuf directly by inclusion in the project file.
* StandaloneProtoCompilationWPF - .netCore 3.1 WPF App, compiling protobuf directly by inclusion in the project file.
* CompilationDummy - .netStandard 2.0 library, compiling protobuf directly by inclusion in the project file.
* ProtobufCompilationOverDummy - .netCore 3.1 Console App, including protobuf by referencing the CompilationDummy project.
* ProtobufCompilationOverDummyWPF - .netCore 3.1 WPF App, including protobuf by referencing the CompilationDummy project.

## What works, what doesn't work?
StandaloneProtoCompilation, ProtobufCompilationOverDummy and ProtobufCompilationOverDummyWPF are working.

StandaloneProtoCompilationWPF does **NOT** work - error message `error CS0246: The type or namespace name 'ProtoDemo' could not be found (are you missing a using directive or an assembly reference?)`
